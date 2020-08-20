<h1>Models</h1>

A model is a Python class that encapsulates all the data. Model is a 
representation of data in the database. Modes are later mapped into a database 
table. A Python Model inherits from class ‘Models’ functionality such as 
ORM - Object Relational Mapping. ORM allows us to interact with databases using 
something called a ‘Manager’ object which is attached to *‘objects’*. 

Model consists of class attributes which, again, are class instances. Those 
attributes define table fields and are responsible for holding and validating 
the correct data type. 

We can create relationships between our models using correct class attributes:

For many to one: 
*models.ForeignKey(NameOfModelThatRepresents’One’, on_delete=models.CASCADE)*

For many to many: 
*models.ManyToMany(NameOfModel)*

Database queries are by default set to **LAZY** meaning that those queries are 
only performed when needed.

Django QuerySets are lazy, which means they are only evaluated when they are 
forced to be. This behavior makes QuerySets very efficient. If you don't set the
QuerySet to a variable, but instead write it directly on the Python shell, 
the SQL statement of the QuerySet is executed because you force it to output 
results.

We can extend our Model functionality by adding class methods (such as __str__) 
or change current behaviour using inner class ‘Meta’. Using Meta class we can, 
for example, change the default sorting order of our queryset (that we receive 
using ORM). 

Managers are attached to Model classes not to instances therefore to receive a 
queryset containing our class instances (database individual records) we can do:

Model.objects.all()

We can look up a individual instance by using ‘get’ and pass a model attribute:

Model.objects.get(attribute=value_we_are_searching_for)

Model managers are not the only managers django uses. When dealing with 
relationships between model's, individual attributes such as "ManyToMany" or 
"ForeignKey" act as managers too. They can be used to access connected instances. 
Relational managers are accessed using model instances not Models itself. 

