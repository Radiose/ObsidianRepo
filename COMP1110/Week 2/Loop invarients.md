Loop invarients
these are the best method to tell if a program is correct. A loop invarient can based off a javadoc 
an example of a javadoc 
```
/**
@param haystack: an array of ints to search for 
@param needle: the integer to search for
@return true iff there exists an i, such that haystack[i] == needle
*/
```
Here you give pre and post conditions, 

therefore
```java
boolean contains(int[] haystack, int needle)
int i = 0
while (i<haystack.length){
	//INV: for all j<1
	//      haystack[j] != needle 
	if(haystack[i]==needle){
		return true
	}
	i=i+1
}
//for all i<haystack.length 
//          haystack[i] != needle
```


This utilises logical reasoning to determine correctness at each step of a loop 

