Pass by [[reference type]]: Pointers 
Pass by value: directly valued - primitive 

record is with lower case - name in upper 

Character.isDigit(char);
Ascii codes:
48 = 0
97 = a

More formally 
If A is a subtype of B 
- The preconditions of A's methods cannot be stronger than B's [[Method]]s
- The Postconditions of A's methods cannot be weaker than the postconditions of B's methods 
- The invariants of B cannot be violated by A
		where we are referring to [[Data invariant]]s
- History constraint - you should not be able to reach a state in the subtype that you wouldnt be able to reach in the supertype through the same sequence of operations 

## Importance
This is very important, often debugging becomes much harder because all code can be working perfectly, but weird behaviour occurs and it becomes difficult to locate why.

Subtyping is also a [[transitive relation]]. If a is a subtype of b, and b is a subtype of c, then a is a subtype of c. 

the most convenient superclass for code reuse is not always the correct one for behaviour subtyping


