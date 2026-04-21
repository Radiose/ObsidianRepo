testing with assert 
```java
void main(String[] args){
	int [] arr1 = new int[]{1,2,3,4,5};
	assert(!contains(arr1,6));
	assert(contains(arr1, 2));	
}
```

running an assertion:
java -ea program.java
If theres a failure, it will tell you if theres a failure.