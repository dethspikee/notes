<h1>Naming and the Environment</h1>

A critical aspect of a programming language is the means it provides for 
using *names* to refer to *computational objects*. A name (a.k.a symbol)
identifies variable whose value is the object. 

In the Scheme dialect we name things with *define*:

```
(define size 3)
```

Above causes the interpreter to associate value "2" with the name "size". 

*Define* is so far the simplest means of abstraction, for it allows us to use
simple names to refer to results of compound operations. Complex programs are 
constructed by building, step by step, computational objects of increasing 
complexity. The interpreter makes this step-by-step program construction
particularly convenient because name-object associations can be created 
incrementally in successive interations.  

It must be clear that possibility of associating values with symbols and later
retrieving them means that the interpreter must maintain some sort of memory
that keeps track of the name-object pairs. This memory is called *environment*
(more precisely the *global environment*, since a computation may involve
a number of different environments).




