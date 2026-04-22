---
aliases:
  - interface
---
a non sealed interface can be implemented wherever, while a [[sealed interface]] can only be implemented where 
Interfaces are [[reference type]]. They serve as a contract. Any [[Class]] that implements an [[non sealed interface|interface]] must implement those methods. 


In this way, a [[Class]] is a subitem of an [[non sealed interface|interface]], or more accurately, a [[Class]] gets put into categories, that are interfaces. 



### Extending an [[non sealed interface|interface]]
Here you add in more methods to the original interface. Its important to note that a [[Class]] can only extend one other class, while it can implement many [[non sealed interface|interface]]s. 

```java
// File: ErasableChatHistory.java
interface ErasableChatHistory extends ChatHistory {
  void erase();
}
```

`erase` is a new method here that isn't in the original ChatHistory interface. 