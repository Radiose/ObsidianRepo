[[dijkstra's algorithm]] in java

To create [[dijkstra's algorithm]], we start off by defining a [[weighted graph]] interface (this will be referred to as a *labelled graph*)

The implementation of [[dijkstra's algorithm]] is essentially just a [[breadth first search]]. The code that's pasted here is very similar to the one that's on the BFS note. 

```java
record PartialRoute(Airport to, List<Airport> steps, int cost)
        implements Comparable<PartialRoute> {
    public int compareTo(PartialRoute o) {
        return Integer.compare(this.cost(), o.cost());
    }
}

List<Airport> routeDijkstra(Airport from, Airport to,
		LabelledGraph<Airport, Integer> routes) {
		
    PriorityQueue<PartialRoute> frontier = new PriorityQueue<>();
    frontier.add(new PartialRoute(from, List.of(from), 0));
    Set<Airport> visited = new HashSet<>();
    while (!frontier.isEmpty()) {
        PartialRoute currentRoute = frontier.poll();
        Airport current = currentRoute.to();
        visited.add(current);
        if (current == to) {
            return currentRoute.steps();
        }
        for (Airport a : routes.adjacent(current)) {
            if (!visited.contains(a)) {
                List<Airport> steps = new ArrayList<>(currentRoute.steps());
                steps.add(a);
                frontier.add(new PartialRoute(a, steps,
                        currentRoute.cost() + routes.label(current, a)));
            }
        }
    }
    return null;
}
```

This code uses a *PriorityQueue* type to create our [[Queue]].  Its not implemented the exact same way as it is in mathematics, but the overall idea is the same. Interestingly, it accomplishes the shortest distance "stupidly". Breadth first search will go from shortest path to longest, so in this way, it will find the shortest [[Path]] first. 