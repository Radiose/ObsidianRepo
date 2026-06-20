---
{}
---
Exception 
Designing your own [[Exception]]s are done using `throw`

When a [[Method]] is asked to do something impossible, you *throw* an [[Exception]].



`throw new IllegalStateException(message)` 
Throwing is not the same as returning something. 
Throwing will return to the caller and to the callers caller all the way up the stack until you reach a *catch*.



You catch an exception via the `try` block.

```java
try {
  g.run(52);
  g.refill(200);
} catch (IllegalStateException e) {
  IO.println("Operation failed (invalid state): " + e.getMessage());
} catch (IllegalArgumentException e) {
  IO.println("Operation failed (invalid argument): " + e.getMessage());
}
```

If nothing catches, the code will crash.  A try block allows for an exception to be handled without crashing the entire code. 


There are some built in exceptions in java

`IllegalStateException`:my private [[COMP1110/Week 6/field]]s aren't in the right state to do what you're asking me to do

`IllegalArgumentException`
You gave me an argument that doesn't make sense - giving a value to a method that doesn't make sense. When an object is in an incorrect state for the requested action. 

Note that you shouldnt try to catch generally.
```java
try {
  account.withdraw(500);
} catch (Exception e) {
  //...
}
```

This will lead to unknown exceptions being handled. Do not try to catch exceptions that you dont know how to handle. 