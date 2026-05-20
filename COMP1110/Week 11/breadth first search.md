Using iterative algorithms that instead are a [[Queue]], it will be **breadth first**.

Breadth first search in particular is a powerful tool. It will check every root exhaustively, starting from the smallest values. This ensures that you will always find the smallest [[Path]].
Importantly, a recursive function does not lend itself well to breadth first search. This is because recursion uses a recursive [[Java call stack and heap|call stack]]. 


```java
List<Airport> routeBFS(Airport from, Airport to, Graph<Airport> routes) {
    Queue<PartialRoute> frontier = new LiamsQueue();
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


