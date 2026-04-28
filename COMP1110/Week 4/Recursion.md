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
### Link to induction 
Note, that similar to [[Induction]], we make an **inductive hypothesis**. We assume that the **result of the recursive call** is correct for all n up to n. 

Recursion is based off executing statements, from beginning to end
each time a recursive function is called, a **frame** is added to the **stack** of variables.
The new frame is **pushed** onto the stack
When the return [[Statement]] is called, the frame is popped from the stack and executed
So it is **built backwards from the stack of frames** until everything is removed from the stack

For each of these stacks, the variables are fixed permanently. 

Developing a binary search recursively

```java
int binarySearch(int[] haystack, int needle,
  int from, int to) {
  if (from >= to) {
    return from;
  }
  int mid = (from + to) / 2;
  if (haystack[mid] == needle) {
    return mid;
  } else if (haystack[mid] < needle) {
    return binarySearch(haystack, needle, mid+1, to);
  } else {
    return binarySearch(haystack,needle,from, mid-1);
  }
```
The inductive hypothesis here is that we assume that the result of the recursive call will be correct. 


Recursion is not without its own problems though. In particular, it has quite average [[space complexity]] and a constant [[time complexity]] of polynomial. The poor space complexity can be attributed to the fact that each call of a recursive function designates another 