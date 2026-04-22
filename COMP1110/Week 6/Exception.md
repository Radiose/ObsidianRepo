---
{}
---
Exception 
Designing your own [[Exception]]s are involved using `throw`

When a [[Method]] is asked to do something impossible, you *throw* and [[Exception]].



`throw new IllegalStateException(message)` 
Throwing is not the same as returning something. 
Throwing will return to the caller and to the callers caller all the way up the stack until you reach a *catch*
If nothing catches, the code will crash 


There are some built in exceptions in java

`IllegalStateException`: my private fields aren't in the right state to do what you're asking me to do

`IllegalArgumentException`
You gave me an argument that doesn't make sense - giving a value to a method that doesn't make sense.