<h1>Reference to an object</h1>

In Python, all values are stored in objects. When you assign a value to a
variable e.g.
```python
    string = "hello"
```

Python creates a new object, places this value (the string "hello" in this case)
inside the new object and then creates a *reference* from the variable name 
*string* to the object. 

Then, if we assign one variable to another, e.g. 
```python 
    new_string = string 
```

Python will create a reference from the new variable *new_string* to the same 
object. 

<h1>Mutable objects and references</h1>

Lists, for example, doesn't store its values inside itself. Instead it stores 
*references* to objects that store values. 

Now, if we assign our list to a new variable and then try to alter the first
object, this will also affect the new list. 


