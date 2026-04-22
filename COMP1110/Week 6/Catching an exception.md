---
{}
---
Catching an exception 
Take the generator [[Class]]. 

```java
Generator gen = new Generator(100);
try{
gen.run(5);
} catch (IllegalStateException e){
	IO.println(e.message());
}
```
This will catch the state expression that is thrown under the `run` method in the generator class