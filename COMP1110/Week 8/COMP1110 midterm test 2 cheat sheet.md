
Examples: 

[[Collection (interface)]]

Making a class immutable is mainly about 
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
- Uninstalling a package will throw the correct error. 
 
MAINTAIN [[Encapsulation]] at all times. When calling from the recursive methods, copy the result of the call into the fourth question


It is very important to remember to read javadocs and questions fully during this test. 
Remember to make fields private when necessary 

Remember to use `this.` 

assertEquals(expected, thingYoureTesting)
