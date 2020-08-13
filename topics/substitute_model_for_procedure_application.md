<h1>Substitute Model for Procedure Application</h1>

To evaluate a combination whose operator names a compound procedure, the 
interpreter follows much the same process as for combinations whose operators 
name primitive procedures. 

That is, the interpreter evaluates the elements of the combination and applies 
the procedure (which is the value of the operator of the combination) to the 
arguments (which are the values of the operands of the combination).

We can assume that the mechanism for applying primitive procedures to arguments
is built into the interpreter. For compound procedures, the application process
is as follows:

* To apply a compound procedure to arguments, evalute the body of the procedure 
  with each formal parameter replaced by the corresponding argument. 

The process we just described is called the **substitution model for procedure 
application**. 

Typical interpreters do not evaluate procedure applications by manipulating 
the text of a procedure to substitute values for the formal parameters.
In practice, the "substitution" is accomplished by using a local environment
for the formal parameters. 

