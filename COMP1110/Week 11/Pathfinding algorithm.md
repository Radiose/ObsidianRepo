
![[Depth first pathfinding algorithm]]


There is also another form of depth first you can create where you use iterative processes. Utilising a [[Stack]] as the data type that contains the set of untested vertices, it is depth first. Using iterative algorithms that instead are a [[Queue]], it will be **breadth first**.

Breadth first search in particular is a powerful tool. It will check every root exhaustively, starting from the smallest values. This ensures that you will always find the smallest [[Path]].
Importantly, a recursive function does not lend itself well to breadth first search. This is because recursion uses a recursive [[Java call stack and heap|call stack]]. 

Note that to create a good [[Pathfinding algorithm]], often you need to use a [[set]] to track whats 'visited'. This prevents [[Cycle graph]]s forming. This isnt needed when working with [[Tree]]s. 


Creating a pathfinding algorithm that works with weights is essentially just implementing [[dijkstra's algorithm]]. This changes the set of untested vertices to be something called a **priority Queue**. A priority queue will order the elements by a particular convention dictated using a [[comparable]] relation definition. 

This can be done as shown below 
```java
record PartialRoute(Airport to, List<Airport> steps, double cost) 

			implements Comparable<PartialRoute>
		{ public int compareTo(PartialRoute other) 
			{ return Double.compare(this.cost, other.cost); 
	} 
}
```