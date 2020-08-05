<h1>Object-Relational Mapping</h1>

Programming languages and database work with data *differently*. There is an
approach called **Object-Relational Mapping** or **ORM** that is able to 
"translate" the database-way of interacting with information in an 
object-oriented way or to translate it backward. 

**Object-Relational Mapping** is a concept of converting data from an
object-oriented programming language to relational database representation 
and vice versa. It solves the problem of matching two different type systems
together and synchronize the data flow between them. 

The main parts of ORM are:
* Virtual tables 
* Relations
* Operations with objects

<h3>Virtual Tables</h3>

Relational databases use tuples and tables to store data. Tuples can be
represented in programming languages but what about tables? 
We can use classes as tables descriptions. We create a class as a virtual table
for the given table in the database. We use or define methods for this class 
to retrieve, change and delete data. 

As you know, a class can have attributes that represent a list of other objects.
For example, a city may have a lot of streets. This link between one object
and several others is called one-to-many relationship. 

<h3>Relations</h3>

The relation is a link that connects a value from one table to the row in
another. When you delete the root row from one table, it can imply cascade 
deletions of all related rows from other tables. 

```
    CITY
   /    \
  /      \
STREET    STREET
```

For example, we can represent above as the class **City** with a list of streets
or as the *many* instances of class **Street** with an atribute *City*. 

**The cascade deletions imply the deletion of dependent objects, not dependent
on ones. For example if you remove city, you will remove it with all the 
appropriate streets. However if you delete the street and it has an attribute
"city", the city will stay in the database.**

<h3>Operations on Objects</h3>

For common operations are known as *CRUD*. Create, read, update and delete 
operations.  
