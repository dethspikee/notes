<h1>Classes</h1>

Classes represent the common structure of similar objects; their data 
and their behaviour. 

<h3>Declaring Classes</h3>

Classes are declared with a keyword *class* and the name of a class:

```python
    class SomeClass:
        var = ... #some variable

        def do_something(self):
            pass 
```

Classes allow you to describe data and behaviours of similar objects. The 
behaviour is called a **method**. Data within classes is stored in the 
**attributes (variables)** and there are two kinds of them: **class attributes**
and **instance attributes**. 

<h3>Class Attributes</h3>

A class attribute is an attribute shared by all instances of the class. 
For example:

```python
    class Book:
        material = "paper"
        cover = "paperback"
        all_books = []
```

All the variables in the class above are *class attributes* and can be 
accessed using the **dot notation** with the name of a class:

```python
    Book.material # paper 

    my_book = Book()
    print(my_book.material) # "paper"
```

**Class attributes** are defined within the class but outside of any methods.
Their value is the same for all instances of that class. 

**Instance variables** store the data unique to each object of the class. 
They're defined with class methods, notably, within the "__init__" method. 


