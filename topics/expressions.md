<h1>Expressions<h1>

Imagine sitting in front of a computer terminal. You type an *expression*,
and the interpreter responds by displaying the result of *evaluating* that
expression.

Expressions representing numbers can be combined with an expression 
representing a primitive procedure (built-in) (such as *&ast;* or *+*) to form
a **compound expression** that represents the application of a procedure 
to those numbers. In other words, *compound expressions* represent procedure
application, for example:

```
(+ 500 200)
700 
```

Expressions such as one above (representing procedure application) are called
*combinations*.

The leftmost element in the list ("+" in the expression above) is called the
*operator* and the other elements are called *operands*. 
The value of a combination is obtained by applying the procedure specified by
the operator to the *arguments* that are the values of the operands. 

Even with complex expressions, the interpreter always operates in the same basic
cycle:

* It reads an expression from terminal
* It evaluates the expression given
* It prints the result of evaluating that expression 

This mode of operation is often described as **REPL**. Read-eval-print-loop. 
