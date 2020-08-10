<h1>Evaluating Combinations</h1>

```
  (* (+ 2 (* 4 6))
     (+ 3 5 7))
```

In evaluating combinations, the interpreter is itself following a procedure.

To evaluate a combination, do the following:

* Evaluate the subexpressions of the combination.
* Apply the procedure that is the value of the leftmost subexpression 
  (the operator) to the arguments that are the values of the other
  subexpressions (the operands). 

First, observe that the first step dictates that in order to accomplish 
the evaluation process for a combination we must first perform the evaluation 
process on each element of the combination. Thus, the evaluation rule is 
*recursive* in nature; that is, it includes, as one of its steps, the need 
to invoke the rule itself. 

Observe that the repeated application of the first step brings us to the point 
where we need to evaluate, not combinations, but primitive expressions such as 
numerals, built-in operators, or other names. We take care of the primitive 
cases by stipulating that:

* the values of numerals are the numbers that they name 
* the values of built-in operators are the machine instruction sequences that 
  carry out the corresponding operations, and 
* the values of other names are the objects associated with those names 
  in the environment

We may regard the second rule as a special case of the third one by stipulating
that symbols such as "+" and "*" are also included in the global environment,
and are associated with the sequences of machine instructions that are their 
"values". 

The key point to notice is the role of the environment in determining the 
meaning of the symbols in expressions. In an interactive language such as Lisp,
it is meaningless to speak of the value of an expression such as (+ x 1) without
specifying any information about the environment that would provide a meaning
for the symbol "x" (or even for the symbol "+"). 

Notice that the evaluation rule given above does not handle *definitions*.
For instance, evaluating *(define x 3)* does not apply the *define* to two 
arguments, one of which is the value of the symbol "x" and the other of which 
is 3, since the purpose of the *define* is precisely to associate "x" wih a 
value. Such exceptions to the general evaluation rule are called **special forms**.
Each special form has its own evaluation rule.

The various kinds of expressions (each with its associated evaluation rule)
constitute the syntax of the programming language. 