
Examples: 

[[Collection (interface)]]
collections written with Set.of() are immutable.
`new TreeSet<>(Set.of(...))` will allow a mutable set 


Making a class mutable involves creating methods that can modify fields of an instance. A class is immutable if the only way to change values involves creating a new object. 
Records are immutable.

remember to check on the specifications for your interfaces. In particular when do they throw exceptions?


if shape = an interface, circle = class, then 
`Shape s = new Circle();`
`s.draw()` will use the circle draw method, provided that the method is outlined in the interface. 



Testing used in practice test 

- the class was empty when initialised (isInstalled returns false)
- installing a package will lead to its dependencies being installed(via javadocs)
-  installing a package will not lead to non dependent packages being installed
 
- data abstraction and encapsulation is maintained. Anything returned does not effect the final result `Set<Package> s = sys.allInstalled();`
	`s.clear()`
	a bunch of other tests. 
	
- The allInstalled method returns an empty set before anything is installed. 
- The allInstalled method returns the packages that were installed into the class 
- uninstalling a package will lead to it being uninstalled 
- Uninstalling a package will lead to things that depend on it being uninstalled 
- Uninstalling a package will not remove things that arent necessary
- Uninstalling a package will throw the correct error when necessary. 
 
MAINTAIN [[Encapsulation]] at all times. When calling from the recursive methods, copy the result of the call into the fourth question


It is very important to remember to read javadocs and questions fully during this test. 
Remember to make fields private when necessary 

Remember to use `this.` 

assertEquals(expected, thingYoureTesting)



BSTs: insert at end of tree, not in middle. (base case is null)

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

TDD:
1. Write a test for the behaviour you want
2. Watch it fail (since there is no implementation yet)
3. Write the minimum implementation to make it pass
4. Repeat

```
Object x = "hello";
String s = (String) x; // cast from Object to String
```

type parameters: <>


```java
public Set<Package> allDependencies() {  
    Set<Package> set = new HashSet<>();  
    set.add(this);  
    for(Package pack : this.directDependencies()){  
            set.addAll(pack.allDependencies());  
    }  
    return set;  
}
```
