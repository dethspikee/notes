<h1>Big O Notation</h1>

We said that time complexity measures how fast an algorithm runs, and space 
complexity measures how much auxiliary memory it takes up. What does it mean?

Different algorithms can run at the similar speed when the input size is small,
however as the input size grows the execution time might change differently. 
This is why we can't measure time complexity in seconds but use a different 
notation such as *Big O*.

The time complexity analysis of an algorithm is a measure of algorithm's speed
or runtime as the size of the input increases. 

Most common cases:
*  O(1) - constant time complexity, as the size of the input increases the
          speed of an algorithm remains constant. 
*  O(n) - linear time complexity, as the size of the input increases the 
          speed of an algorithm increases linearly (we're going to have to
          traverse through every value in the list for example). 
*  O(n<sub>2</sub>) - time directly proportional to the square of the input size 

What unit are we dealing with?

The unit that we use for time complexity is **elementary operation**.

Accessing a value in an array at a given index would take constant time. 

When we are analysing the behaviour of an algorithm given input N when N 
tends toward infinity, we don't really care about exact number of elementary 
operations that we are going to be performing so long as that number doesn't 
have a relationship to the size of input N. 

