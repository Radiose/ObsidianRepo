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

We can also create an iterative version. This version prevents [[Stack overflow]] errors, 

```java
record PartialRoute(Airport to, List<Airport> steps) {}

List<Airport> routeDFS(Airport from, Airport to, Graph<Airport> routes) {
    Stack<PartialRoute> frontier = new LiamsStack<>();
    frontier.add(new PartialRoute(from, List.of(from)));
    Set<Airport> visited = new HashSet<>();
    while (!frontier.isEmpty()) {
        PartialRoute currentRoute = frontier.next();
        Airport current = currentRoute.to();
        visited.add(current);
        if (current == to) {
            return currentRoute.steps();
        }
        for (Airport a : routes.adjacent(current)) {
            if (!visited.contains(a)) {
                List<Airport> steps = new ArrayList<>(currentRoute.steps());
                steps.add(a);
                frontier.add(new PartialRoute(a, steps));
            }
        }
    }
    return null;
}
```
Note that `LiamsStack` is an explicit stack. 
The basics of this algorithm is that `frontier` is all routes that we *havent* tried yet