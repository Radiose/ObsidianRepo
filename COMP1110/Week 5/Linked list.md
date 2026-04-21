Linked list 
Has two parts - head and tail - first element and rest of the list 
This is an example of a *recursive datatype*
```java
record StudentRoll(Student head, Grade grade){};
StudentRoll roll = new StudentRoll(stu, new StudentRoll(stu2, new StudentRoll)(stu3, null));
```
This linked list works similarly to how lists work in **Haskell**. Because this is a recursive datatype, the best method to work with it is to utilise [[Recursion]].
```java
void printAllStudents(StudentRoll students){
if (students == null)
	IO.println("Done");
else
	Student hd = students.head();
	Student tl = students.tail();
	printSummary(hd);
	printAllStudents(tl);	
}
```
Keep in mind that all recursive functions have the risk of [[Stack overflow]]. In the case above, you can use loops for a more memory efficient option.

```java
void printAllStudents(StudentRoll students){
	while(students != null){
		printSummaries(Students.head());
		students = students.tail();
	}	
	IO.println(Done);
}
```

inserting items into a linked loop

```java
StudentRoll insertStudent(Student stu, StudentRoll roll){
	if (roll == null)
		return new StudentRoll(stu, null);
	else{
	int c = stu.name().compareTo(roll.head().name());
		if (c<0)
			return new StudentRoll(stu, roll);
		else if( c>=0){
			StudentRoll newTail = insertStudent(stu, roll.tail())
			return new (StudentRoll(roll.head(), newTail));
		}
	}
}
```
This somewhat complicated looking function will recursively iterate through StudentRoll, until `stu` is alphabetically tested until the correct location for insertion is found. *Precondition* being that the roll is already pre sorted alphabetically.

Implementing binary search 
```java
record FastRoll(Student head, FastRoll left, FastRoll right){}
FastRoll insert(Student stu, FastRoll roll){
	//base case
	if (roll == null){
	return new FastRoll(stu, null, null)
	}else{
		int c = stu.name.compareTo(roll.head.name);
		if (c < 0){
			FastRoll newLeft = insert(stu, roll.left());
			return new fastRoll(roll.head(), newLeft, roll.right())
		else
			FastRoll newRight = insert(stu, roll.right())
			return new FastRoll(roll.head(), newRight, )
	} 
	}
}
```

newLeft and newRight are recursive calls, where the result of this will be an insertion in the bottom of the binary tree .


Lookup functions 
```java
Grade lookup(String name, FastRoll roll) {
  if (roll == null) {
    return null;
  }
  
  int c = name.compareTo(roll.head().name());
  if (c < 0) {
    return lookup(name, roll.left());
  } else if (c == 0) {
    return roll.head().grade();
  } else {
    return lookup(name, roll.right());
  }
}
```


using a looped version 
```java
Grade lookupLoop(String name, FastRoll roll) {
  while (roll != null) {
    int c = name.compareTo(roll.head().name());
    if (c == 0) {
      return roll.head().grade();
    } else if (c < 0) {
      roll = roll.left();
    } else {
      roll = roll.right();
    }
  }
  return null;
}
```
Keep in mind that the `lookup` function can be turned into a loop, because theres no actual modification to the list structure. Its simply utilising the loop to search. 

On the other hand the `insert` function *cannot* be turned into a loop, because the current [[Record]] structure that we have is immutable.,

