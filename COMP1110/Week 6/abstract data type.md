---
{}
---
abstract data type 

An ADT is defined solely by its [[non sealed interface|interface]]. The implementation is irrelevant. 
The generator class 
```java
class Generator{
//creating an object with a constructor
	int fuel;
	int capacity;
	Generator(int capacity){
	//add methods to generator 
	
	//this classes capacity (outside brackets) is the capacity in the constructor 
	this.capacity = capacity;
	this.fuel = capacity;
	}
	void run(int hour){
	
	}
	void refill(int fuel){
	
	}
	
}
```

is an example of an abstract data type. 

The class generator has its own methods (run, refill), you can call the methods, interact with them, but thats it. You dont have to see how its done. This is all because of [[Abstraction]].
