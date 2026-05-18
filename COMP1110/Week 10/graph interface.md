[[graph]] [[non sealed interface|interface]]

```java
public interface Graph<V> {
    void addVertex(V vertex);
    void connect(V from, V to);
    boolean isConnected(V from, V to);
    Set<V> adjacent(V from);
    int numVertices();
}
```


Creating a [[Class]] that implements it 
```java
public class AdjacencyListGraph<V> implements Graph<V> {
    Map<V, Set<V>> adjacencies;

    AdjacencyListGraph() {
        this.adjacencies = new HashMap<>();
    }

    public void addVertex(V vertex) {
        this.adjacencies.put(vertex, new HashSet<>());
    }

    public void connect(V from, V to) {
        if (!this.adjacencies.containsKey(from) 
         || !this.adjacencies.containsKey(to)) {
            throw new IllegalArgumentException("vertex doesn't exist");
        }
        this.adjacencies.get(from).add(to);
    }

    public boolean isConnected(V from, V to) {
        if (!this.adjacencies.containsKey(from) 
         || !this.adjacencies.containsKey(to)) {
            throw new IllegalArgumentException("vertex doesn't exist");
        }
        return adjacencies.get(from).contains(to);
    }

    public Set<V> adjacent(V from) {
        return new HashSet<>(this.adjacencies.get(from));
    }

    public int numVertices() {
        return this.adjacencies.size();
    }
}
```

This implementation has a private [[field]] that is a HashMap mapping [[Adjacent vertices]], via mapping a vertex to its [[set]] of adjacent vertices. 

This has weaknesses though, using .contains has bad [[time complexity]] (O(n)). isConnected is slow then. 

Creating an [[Adjacent vertices|adjacent matrix]] [[Class]]
```java
public class AdjacencyMatrixGraph<V> implements Graph<V> {
    boolean[][] connected;
    Map<V, Integer> indices;
    int size;

    AdjacencyMatrixGraph() {
        this.connected = new boolean[100][100];
        this.indices = new HashMap<>();
        this.size = 0;
    }

    public void addVertex(V vertex) {
        if (this.size == 100) throw new RuntimeException("out of space");
        this.indices.put(vertex, this.size);
        this.size = this.size + 1;
    }

    public void connect(V from, V to) {
        if (!this.indices.containsKey(from) || !this.indices.containsKey(to)) {
            throw new IllegalArgumentException("vertex doesn't exist");
        }
        this.connected[this.indices.get(from)][this.indices.get(to)] = true;
    }

    public boolean isConnected(V from, V to) {
        if (!this.indices.containsKey(from) || !this.indices.containsKey(to)) {
            throw new IllegalArgumentException("vertex doesn't exist");
        }
        return this.connected[this.indices.get(from)][this.indices.get(to)];
    }

    public Set<V> adjacent(V from) {
        Set<V> set = new HashSet<>();
        for (V vertex : this.indices.keySet()) {
            if (this.isConnected(from, vertex)) set.add(vertex);
        }
        return set;
    }

    public int numVertices() {
        return this.indices.size();
    }
}
```
This implementation will utilise indices as a map between a vertex and a row/column, just like in a real [[Adjacent vertices|adjacent matrix]]. *Note, this implementation is for a [[directed graphs|digraph]].* If we use a regular [[graph]], we can store these values in half the size(symmetric matrix is useless)
You could make this labelled, for example contain things like airline ticket prices between vertices. Then you change the type of the array to `int`

Size is a tracker to make sure it stays within the size of the array(100), and if it exceeds that, it will throw an [[Exception]]
For this complexity: isConnected is just an array lookup with complexity of (O(1))
Adjacent is O(V), and the backing array always occupies $O(V^2)$ complexity

An edge list is simply a list of all edges. It has a complexity of O(n