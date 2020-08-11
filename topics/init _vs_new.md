<h1>__init__ vs __new__</h1>

New objects are initialized with the \__init__ method but they are created 
by the *\__new__* method that in its turn calls the \__init__ method. 

The first argument to \__new__ is "cls". It represents the class itself, 
similar to how *self* represents an instance of the class. The method returns 
a new instance of a class which is then passed to the *\__init__* method. 

