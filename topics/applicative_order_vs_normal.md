<h1>Applicative order versus normal order</h1>

According to the description of evaluation, the interpreter first evaluates 
the operator and operands and then applies resulting procedure to the 
resulting arguments. This is not the only way to perform evalutions. 

An alternative evaluation model would not evaluate operands until their 
values were needed (in other words, when the value of the operator would be 
a primitive operation). 

This alternative "fully expand and then reduce" evaluation method is known as 
*normal-order evaluation*, in contrast to the "evaluate the arguments and then
apply" method that the interpreter actually uses, which is called 
*applicative-order evaluation*. 

