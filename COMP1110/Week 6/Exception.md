---
{}
---
Exception 
`throw new IllegalStateException(message)` 
Throwing is not the same as returning something. 
Throwing will return to the caller and to the callers caller all the way up the stack until you reach a *catch*
If nothing catches, the code will crash 

IllegalStateException: my private fields arent in the right state to do what youre asking me to do
IllegalArgumentException
You gave me an argument that doesn't make sense - giving a value to a method that doesn't make sense.