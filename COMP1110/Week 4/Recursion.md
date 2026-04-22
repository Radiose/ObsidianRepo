---
{}
---
Recursion
Recursion in java is done similarly to how its done in *Haskell*
Its based off of underlying principles done in mathematical [[Induction]]
Two main items needed to execute correctly
A base case - 
- How does the program know when to stop recursion? What happens when it stops.
- This should always be checked first when writing a program
An inductive (recursive) case
- What should the program do if it isn't the base case?
- How does the program move towards the base case(stopping the recursion)
Recursion
is based off executing statements, from beginning to end
each time a recursive function is called, a **frame** is added to the **stack** of variables.
The new frame is **pushed** onto the stack
When the return [[Statement]] is called, the frame is popped from the stack and executed
So it is **built backwards from the stack of frames** until everything is removed from the stack

For each of these stacks, the variables are fixed permanently. 

Developing a binary search recursively

```java
int binarySearch (int[] haystack, int needle, int from, int to){
int mid = (from+to) /2 ;

if (from >= to)
	return from;

else if (haystack[mid] < needle)
	return(binarySearch(haystack, needle, mid+1, to));	
else
	return(binarySearch(haystack, needle, from, mid-1));
}
```
