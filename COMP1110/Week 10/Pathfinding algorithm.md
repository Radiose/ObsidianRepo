
![[Depth first search]]


Note that to create a good [[Pathfinding algorithm]], often you need to use a [[set]] to track whats 'visited'. This prevents [[Cycle graph]]s forming. This isnt needed when working with [[tree]]s.
![[breadth first search]]

Creating a pathfinding algorithm that works with weights is essentially just implementing [[dijkstra's algorithm]] . This changes the set of untested vertices to be something called a **priority Queue**. A priority queue will order the elements by a particular convention dictated using a [[comparable]] relation definition. 

![[dijkstra's algorithm in java]]
