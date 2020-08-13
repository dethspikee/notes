<h1>Compound Procedures</h1>

We have identified some of the elements that must appear in any powerful 
programming language:

* Numbers and arithmetic operations are primitive data and primitive 
  procedures 
* Nesting of combinations provides a means of combining operations 
* Definitions that associate names with values provide a limited means of 
  abstraction. 

**Procedure definition** is a powerful abstraction technique by which a 
compound operation can be given a name and then referred to as a *unit*. 

```
(define (square x) (* x x)) 
``` 

Evaluating this definition creates this compound procedure and associates 
it with the name *square*. 

The general form of a procedure definition is:

```
(define (<name> <formal parameters>) (body))
``` 

The <name> is a symbol to be associated with the procedure definition in 
the environment. The <formal parameters> are the names used within the body 
of the procedure to refer to the corresponding arguments of the procedure. 
The <body> is an expression that will *yield* the value of the procedure 
application when the formal parameters are replaced by the actual arguments 
to which the procedure is applied. 