---
{}
---
Class 
A class is a key part of **object orientated programming**. The idea of object orientated programming is that we want the types in our program to model actual things. The capabilities of an object is defined as its [[Method]]s. We use classes to model the real world as a system of classes that interact with each other through methods. A [[Class]] is often an implementation of an [[non sealed interface|interface]]


A class that implements a [[sealed interface]] must be declared as either `final class`, ``
`sealed class` or `non sealed class`.

defining a class in java

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



```java
interface ErasableChatHistory extends ChatHistory{
void erase(){

}
}
``` 


