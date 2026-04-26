collection (interface)
An [[non sealed interface|interface]] defined as a collection of elements. Is the most general form of any interfaces implemented through `<>` in java. 

Implemented through `<>`. 
So, `public interface GuestList <T>` can be thought of as `public interface GuestList <T> extends Collection<T>`


### Methods
here I will list methods that typically need to be called directly to `collections`
`Collections.sort` - uses **tim sort**,  a [[Sorting algorithm]] that is an interesting hybrid between [[Merge sort]] and other $O\ (n \ log(n))$ algorithms 
collections.addAll();
This is how you add other collections to a collections. 