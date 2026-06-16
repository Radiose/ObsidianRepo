The expression problem 
in a programming language, you can make it easy to do one of two things 
1: Add new types of data to existing operations
	In functional - go through every operation that just implemented and add something to it - hard 
2: add new operations to existing types of data 
	In an OOP, this is quite tricky. We have to add a method to an interface, and go to every implementing class of that interface to have that new operation 
	In a functional programming language - this is easy 

For example 

```java
sealed interface Person permits Student, Staff {}
record Student(String name, String uid) implements Person;
Records Staff(String name, String position) implements Person;

String name(Person p){
switch(p){
case Student(String name, String uid) ->{ 
	return name;
		}
case Staff(String name, String position) -> {
		return name;
		}
	}
}

```
Adding another Person is hard, as we would need to the switch 
Adding a new operation is easy 

For an OOP - adding another person is easy - make another class 
Adding a new operation is hard 

Functional approach is slower sometimes but has many other advantages

