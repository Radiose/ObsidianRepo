Its quite difficult to ensure that we have subtyping relationships that are valid behavioural subtypes.

Whenever we have a subtype that uses a supertype. If we make it a subtype instead a supertype, all behaviour of that class should remain the same. 
IE if Gardener extends worker, then if we replace the worker class with gardener, you should get the same outputs. 

So - you should only use inheritance when there is no difference in behaviour - otherwise theyre too different and subclassing is not appropriate.

Informally:
Every time a supertype is used, can a subtype be substituted and the same behaviour be found?


More formally 
If A is a subtype of B 
- The preconditions of A's methods cannot be stronger than B's [[Method]]s
- The Postconditions of A's methods cannot be weaker than the postconditions of B's methods 
- The invariants of B cannot be violated by A
		where we are referring to [[Data invariant]]s
- History constraint - you should not be able to reach a state in the subtype that you wouldnt be able to reach in the supertype through the same sequence of operations 

## Importance
This is very important, often debugging becomes much harder because all code can be working perfectly, but weird behaviour occurs and it becomes difficult to locate why.
