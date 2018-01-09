## Shortest Path Algorithm for Negative Edge Costs

- [Upper Level](README.md)

```c++
// Pseudocode
void Graph::weightedNegative(Vertex s) {
  Queue<Vertex> q;
  
  for each Vertex v
    v.dist = INFINITY;
  
  s.dist = 0;
  q.enqueue(s);
  
  while (!q.isEmpty()) {
    Vertex v = q.dequeue();
    
    for each Vertex w adjacent to v
      if ((v.dist + cvw) < w.dist) {
        w.dist = v.dist + cvw;
        w.path = v;
        if (w is not already in q)
          q.enqueue(w);
      }
  }
}
```

The algorithm costs O(\|E\|x\|V\|) time.