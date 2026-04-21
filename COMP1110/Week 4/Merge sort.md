Merge sort 
A [[Sorting algorithm]]

Computing based 
A merge [[Function]] is one that takes in two pre sorted lists and returns a merged list of both combined

Merge sort is a **not [[In place algorithm]]** 

the basic merge algorithm:
```java
int[] merge(int[] left, int[] right) {
  int i = 0;
  int j = 0;
  int k = 0;
  int[] output = new int[left.length + right.length];
  while (i < left.length && j < right.length) {
    if (left[i] <= right[j]) {
      output[k] = left[i];
      i = i + 1;
    } else {
      output[k] = right[j];
      j = j + 1;
    }
    k = k + 1;
  }
  //when one loop is greater than the other
  while (i < left.length) {
    output[k] = left[i];
    i = i + 1;
    k = k + 1;
  }
  while (j < right.length) {
    output[k] = right[j];
    j = j + 1;
    k = k + 1;
  }
  return output;
}
```

Now the actual loop to utilise this as shown
```java
int[] sort(int[] input, int start, int end) {
 //base cases 
 //start and end mixed up - return empty
 if (end < start) {
   return new int[]{};
 } //start and end equal - singular element in array - return the element 
 else if (end == start) {
   return new int[]{input[start]};
 } 
 //inductive case - recursively keep breaking up list into smaller and smaller sublists
 else {
   int mid = (start + end) / 2;
   int[] left = sort(input,start,mid);
   int[] right = sort(input,mid+1,end);
   return merge(left,right);
 }
}
```
Note that because there is no base case checking mid, one of the left/right indexes must contain the original mid. In a binary search, this is not important as we are purely testing for equality.
