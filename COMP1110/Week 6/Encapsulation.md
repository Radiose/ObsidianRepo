Encapsulation
We are hiding the fields, and just showing a [[Method]] to the outside world. 

This is important for two main reasons. 

**Integrity** -we maintain data invariants about an objects internal state 
	data invariants are properties that should be true before and after each call of a [[Method]] on an object 
**Abstraction** - we can separate the [[non sealed interface|interface]](what methods are exposed to the public) from the implementation(private fields). This means users only need to know about the interface, reducing cognitive load on programmers. This is essential for large programming projects. It also enables flexibility. 