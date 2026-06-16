Pass by [[reference type]]: Pointers 
Pass by value: directly valued - primitive 

record is with lower case - name in upper 

Character.isDigit(char);
Ascii codes:
48 = 0
97 = a

More formally 
If A is a subtype of B 
- The preconditions of A's methods cannot be stronger than B's [[Method]]s
- The Postconditions of A's methods cannot be weaker than the postconditions of B's methods 
- The invariants of B cannot be violated by A
		where we are referring to [[Data invariant]]s
- History constraint - you should not be able to reach a state in the subtype that you wouldnt be able to reach in the supertype through the same sequence of operations 

## Importance
This is very important, often debugging becomes much harder because all code can be working perfectly, but weird behaviour occurs and it becomes difficult to locate why.

Subtyping is also a [[transitive relation]]. If a is a subtype of b, and b is a subtype of c, then a is a subtype of c. 

the most convenient superclass for code reuse is not always the correct one for behaviour subtyping




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


Important recursive functions: 
```java
public int maxDepth() {  
    List<Integer> lst = new ArrayList<>();  
    int maxNo = 0;  
    if(this.replies().isEmpty()){  
        return 1;  
    }  
    else{  
        for(Comment reply : this.replies()){  
            if(1 + reply.maxDepth() > maxNo){  
                maxNo = 1+ reply.maxDepth();  
            }  
        }  
        return maxNo;  
    }  
}
```

```java
public record FamilyTree(String name, Set<FamilyTree> children) {  
    private FamilyTree getLargestNode(){  
        FamilyTree largestNode = this;  
        if(this.children.isEmpty()){ return largestNode;}  
  
        for(FamilyTree child : this.children){  
            if(child.getLargestNode().children.size() > largestNode.children.size()){  
                largestNode = child.getLargestNode();  
            }  
        }  
        IO.println(largestNode.name());  
        return largestNode;  
    }  
  
    public String mostChildren() {  
        //Hint: you may find it useful to write a private helper method that  
        // returns a FamilyTree node rather than a String.        return getLargestNode().name;  
    }  
}
```

Issues have been that `largestNode = child.getLargestNode` needs to be used. 

[[Queue]]: FIFO
Stack:  FILO
