<h1>Local Names, scope, bound and free variables</h1>

One detail of a procedure's implementation that should not matter to the user 
of the procedure is the implementer's choice of names foe the procedure's 
formal parameters. Thus, the following procedures should not be 
distinguishable:

```
    (define (square x) (* x x))

    (define (square y) (* y y))
```

Parameter names of a procedure must be local to the body of a procedure. 

A formal parameter of a procedure has a very special role in the procedure 
definition, in that it doesn't matter what name the formal parameter has. 
Such a name is called a **bound variable**, and we say that the procedure 
definition *binds* it formal parameters. If a variable is not bound, we say 
that it is **free**. The set of expressions for which a binding difines a name 
is called the **scope** of that name. 

In a procedure definition, the bound variables declared as the formal parameters
of the procedure have the body of the procedure as their scope. 

