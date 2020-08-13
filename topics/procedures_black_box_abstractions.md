<h1>Procedures as a Black-Box Abstractions</h1>

Take a look at procedures below:

```
   (define (sqrt x)
        (sqrt-iter 1.0 x)) 
```

"Sqrt" is an example of a process defined by a set of mutually defined procedures.
The entire sqrt program can be viewed as a cluster of procedures that mirrors 
the **decomposition** of the problem into subproblems. 

The importance of this decomposition strategy is not simply that one is dividing
the program into parts. Rather, it is crucial that each procedure accomplishes
an identifiable task that can be used as a module in defining other procedures. 

For example, users of "sqrt" doesn't have to know how "sqrt-iter" works, it can
act as a "black-box". It is a *procedural abstraction*. 


