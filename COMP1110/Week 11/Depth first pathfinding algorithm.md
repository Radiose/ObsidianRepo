Depth first pathfinding algorithm 
This is a [[Recursive backtracking]] algorithm goes all the way down the bottom of the [[Tree]] until it reaches a leaf, and then does the next leaf etc. [[Recursion]] naturally lends itself to depth first traversals.

```java
enum Airport { SYD, MEL, BNE, PER, ADL, CBR }

List<Airport> route(Airport from, Airport to, Graph<Airport> routes, Set<Airport> visited) {
    visited.add(from);
    if (from == to) {
        return List.of(from);
    }
    for (Airport child : routes.adjacent(from)) {
        if (!visited.contains(child)) {
            List<Airport> r = route(child, to, routes, visited);
            if (r != null) {
                List<Airport> ret = new ArrayList<>();
                ret.add(from);
                ret.addAll(r);
                return ret;
            }
        }
    }
    return null;
}
```
This is an example of depth first being implemented using an implicit [[Stack]], ie the callstack thats present in [[Recursion]].

We can also create a 