<h1>Block Structure and Lexical Scoping</h1>

We have one kind of name isolation available so far: formal parameters 
of a procedure are local to the body of the procedure. Program below consists of 
separate procedures:

```
    (define (sqrt x)
        (sqrt-iter 1.0 x))
    
    (define (sqrt-iter guess x)
        (if (good-enough? guess x)
            guess
            (sqrt-iter (improve guess x) x)))

    (define (good-enough? guess x)
        (< (abs (- (square guess) x)) 0.001))
    
    (define (improve guess x)
        (average guess (/ x guess)))
```

The problem with this program is that the only procedure that is important to 
users of "sqrt" is "sqrt". The other procedures only clutter up the namespace.
The problem is severe in the construction of large systems where there might be 
several procedures with the same name. 

We can use *block structure* to define internal definitions to solve
name-packaging problems. In addition to nested definitions we can take advantage
of "x" being a bound variable to "sqrt" procedure definition meaning that all 
internal/nested definitions are in scope of x. This discipline is called 
*lexical scoping*. 

*Lexical Scoping* defines that free variables in a procedure are taken to refer 
to binding made by enclosing procedure definitions; that is, they're looked up
in the environment in which the procedure was defined. 

```
    (define (sqrt x)
        (define (goood-enough? guess)
            (< (abs (- (square guess) x)) 0.001))
        (define (improve guess)
            (average guess (/ x guess)))
        (define (sqrt-iter guess)
            (if (good-enough? guess)
            guess 
            (sqrt-iter (improve guess))))
        (sqrt-iter 1.0))
```