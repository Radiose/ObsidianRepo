Inheritance
Inheritance refers to allowing one [[Class]] to act as an extension of another. It can be done directly via the `extends` keyword. Inheritance is conceptually similar to [[non sealed interface|interface]]s, except that [[Method]]s dont have to to be implemented as they are already implemented in the other class. 

### Terminology
Subclass - the class that inherits
superclass - the class that is being extended

An important thing to note is that constructor methods are not inherited. 

@Override is a keyword that you can use to override the superclass implementation. 

Why to avoid inheritance?
Coupling is a measure of quality of design. If two parts of a project are highly coupled, changes to one of them greatly affects the others. Whenever we make changes to a superclass, we must consider the subtypes. 
Another reason - its quite difficult to ensure that we have subtyping relationships that are valid behavioural subtypes 
Behavioural subtypes- whenever we have a subtype that uses a supertype. If we make a supertype instead a subtype, all behaviour of that class should remain the same. 
IE if Gardener extends 