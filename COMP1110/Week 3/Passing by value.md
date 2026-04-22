---
{}
---

When a function is run, it creates something called a *frame*, a storage space set aside for the local variables that are run inside that function. The values of the arguments given in the functions call are copied into the functions frame.
When the function returns, the frame is no longer needed, and is destroyed. 

```java
void baz(int x) {
  x = x + 1;
}
void main(String[] args) {
  int[] arr = new int[]{1,2,3,4,5};
  baz(arr[0]);
  IO.println(arr[0]);
}
```
This function above, will print 1. What occurs here, is that a new variable x is created in baz, one more is added, with its original value the same as arr\[0]. Then, the frame is destroyed. 
The x does not carry through. A copy of the first element is created. 

![[Value type]]

In contrast, arrays are examples of reference types 
![[reference type]]