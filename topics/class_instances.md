<h1>Class Instances</h1>

A class instance is an object of the class. Initially all instances of the class
would be identical to one another. Most of the time it's not what we want.
To customize initial state of an instance, the **\__init__** method is used. 

The *\__init__* method is used to **initialize** the instance. A class can have 
only one \__init__ method. If *\__init__* is defined within a class it is 
automatically invoked when we create a new class instance. 

```python
class River:
    # list of all rivers
    all_rivers = []
    
    def __init__(self, name, length):
        self.name = name
        self.length = length
        # add current river to the list of all rivers
        River.all_rivers.append(self)

volga = River("Volga", 3530)
seine = River("Seine", 776)
nile = River("Nile", 6852)

# print all river names
for river in River.all_rivers:
    print(river.name)
# Output:
# Volga
# Seine
# Nile
```

<h3>self</h3>

The **self** argument represents a particular instance of the class and allows 
us to access its attributes and methods. 

Most of the time we also need to write *self* parameter in other methods 
because when the method is called the first argument that is passed to the 
method is the object itself. Example

```python
    class River:
    all_rivers = []

    def __init__(self, name, length):
        self.name = name
        self.length = length
        River.all_rivers.append(self)

    def get_info(self):
        print("The length of the {0} is {1} km".format(self.name, self.length))
``` 

Produces the following output:

```python
    volga.get_info()
    # The length of the Volga is 3530 km
    seine.get_info()
    # The length of the Seine is 776 km
    nile.get_info()
    # The length of the Nile is 6852 km
``` 

As you can see, for each object the *get_info()* method printed its particular 
values and that was possible because we used the **self** keyword in the method.

Note that when we actually call an object's method we don't write the *self*
argument in the brackets. The *self* parameter (that represents a particular
instance of the class) is passed to the instance method **implicitly** when
it's called. There are actually two ways to call and instance method: 
*self.method()* or *class.method(self)*:

```python 
    # self.method()
    volga.get_info()
    # The length of the Volga is 3530 km

    # class.method(self)
    River.get_info(volga)
    # The length of the Volga is 3530 km
```

<h3>Instance Attributes</h3>

Instance attributes are defined within methods they store instance-specific 
information. 

Instance attributes are available only from the scope of the object. 
