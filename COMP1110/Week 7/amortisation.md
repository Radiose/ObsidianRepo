amortisation 
This is a form of reducing [[time complexity]] of an algorithm.

Eg, for an [[Array]] that needs to be increased as time goes on
```java
void add (String name, String[] arr, int count)if (count==arr.length()){
	String[] old = arr ;
	arr = new String[arr.length * 2];
	//copy old into arr 
	}
```
