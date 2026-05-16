Queue
Implemented in java with an [[abstract data type]]
[[Method]]s needed: Add to queue 
Size of queue 
boolean isEmpty()

Queues are FIFO - first person to line up is the first person to leave 
The ideal structure for implementing this is an `ArrayList` from the [[List (collection)]]. 

Below is a very basic implementation of a queue:
```java
public class LiamsQueue implements Queue<String> {
    ArrayList<String> q;

    LiamsQueue() {
        this.q = new ArrayList<>();
    }

    public void add(String input) {
        q.add(input);
    }

    public String next() {
        if (q.isEmpty()) {
            return null;
        }
        String s = q.getFirst();
        q.removeFirst();
        return s;
    }

    public int size() { return q.size(); }
    public boolean isEmpty() { return q.isEmpty(); }
}
```

This above is quite inefficient, mainly because it uses removeFirst method. It has poor complexity. A better method would be to use [[amortisation]].

