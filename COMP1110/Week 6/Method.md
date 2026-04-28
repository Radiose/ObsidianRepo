---
{}
---
Method 
Sometimes when you call a function, such as [[String equality]], **.equals** is a method.
The way we make [[Method]]s is by putting it in the curly braces when we make custom data types 

```java
record Generator (int fuel, int capacity){
	Generator run(int hours){
	int fuelNeeded = hours * 5
	if(this.fuel()>fuelNeeded){
		return new Generator(this.fuel()-fuelNeeded, this.capacity())
	}
	}
}

void main(String[] args){
g = new Generator(50,100);
g2 = g.run(5);
}
```

A method is a function associated with a particular object.

