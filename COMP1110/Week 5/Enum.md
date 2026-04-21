Enum 
a type that represents numbers
When creating types, you want to minimise the amount of possible values for that type 
So for something that should only output numbers 1-4 inclusive, its better to only have that a type that can have 1-4 instead of the type `int`  

#### Declaring enum types 

```java
enum Grade{
	P,
	Cr,
	D,
	HD,
	PX,
	N
}
void main(String[] args){
	int mark = Integer.parseInt(args[0]);
	Grade g;
	if (mark < 40){
	g = Grade.N;
	} else if (mark < 50)
		g  = Grade.PX
	else if(mark < 60)
		g = Grade.Cr
	else if(mark < 70)
		g = Grade.D
	else
		g = Grade.HD
}

```

Like Strings, enums are pass by reference. HOWEVER, you can treat it like pass by value. This is because the only possible locations in memory are the ones in the type, unlike string which can have a different location in memory for every single string.