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


Creating a class that implements AdjacencyList