<h1>\__str__ vs \__repr__</h1>

*\__str__* defines the behaviour of a *str()* function and *\__repr__* defines 
the *repr()* function. A general rule is that the output of the "\__str__"
should be highly visible (create representation for users) and output for a 
"\__repr__" should be unambiguous (create representation for developers)

Both should return string object.

\__repr__ is also a fallback to a \__str__ if a latter is not defined. 

