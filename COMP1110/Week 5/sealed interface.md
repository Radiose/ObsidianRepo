---
{}
---
Different to a [[non sealed interface]]

A way to group several types together under a single type.
This is an example of an **algebraic datatype**


```java
enum Level{UG,PG}
enum Pos{PROFF, APRO, SEN_LEC, LEC}
record Student(int uid, String name, Level level) {}
record Staff (int uid, String name, Position pos) {}

sealed interface Person permits Student, staff {}

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
this sealed interface creates a type person, that will either be a student or staff.


The biggest difference between a sealed and [[non sealed interface]], is that a sealed interface can only be implemented where permitted (`permits Student, Staff`).