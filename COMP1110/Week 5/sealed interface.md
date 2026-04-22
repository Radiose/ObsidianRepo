---
{}
---
Different to a [[non sealed interface]]

A way to group several types together under a single type.
This is an example of an **algebraic datatype**

*Sealed* interfaces allow for grouping of *records* together. This is different to a [[Record]], as a record groups together under the AND [[logical connective]]. Sealed interfaces group together under the OR. 


```java
sealed interface Shape permits Rectangle, Triangle, Circle {}
record Rectangle(int w, int h) implements Shape {}
record Triangle(int a, int b, int theta) implements Shape {}
record Circle(int r) implements Shape {}
```
A shape can be either a rectangle OR a triangle OR a circle. 



```java
enum Level { UG, PG }

enum Position { PROFESSOR, APRO, SEN_LEC, LEC }

sealed interface Person permits Student, Staff {}

record Student(int uid, String name, Level level)
  implements Person {}

record Staff(int uid, String name, Position pos)
  implements Person {}


void greet(Person p) {
switch (p){
	case student(uid, name, level) ->
		IO.println("hello " + name);
	case staff(uid, name, pos) ->
		switch(pos){
			case PROFF -> IO.println("Professor");
			case APRO -> IO.println("Associate professor");
			default -> IO.println("Dr.");
			}
	}
}
```
this sealed interface creates a type person, that will either be a student or staff. Each record implements the interface, and the sealed interface permits each record to implement it. 

The biggest difference between a sealed and [[non sealed interface]], is that a sealed interface can only be implemented where permitted (`permits Student, Staff`).

```java
sealed interface BoolExpr permits Constant, Variable, And, Or, Not {}

record Constant(boolean value) implements BoolExpr {}

// the char must be a lowercase letter
record Variable(char name) implements BoolExpr {}

record And(BoolExpr left, BoolExpr right) implements BoolExpr {}
record Or(BoolExpr left, BoolExpr right) implements BoolExpr {}
record Not(BoolExpr e) implements BoolExpr {}
```
Here is an example of a recursive data type. 

This sealed interface `BoolExpr` is a category that Constant, Variable... Not are a part of. 

Each of the record types contain another BoolExpr within them. BoolExpr can be one of the Constant, Variable...Not.

