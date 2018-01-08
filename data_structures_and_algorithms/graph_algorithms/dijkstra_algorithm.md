## Dijkstra's Algorithm

- [Upper Level](README.md)

#### Weighted Shortest Path

- Prerequisite: All edges in the graph are positive.

```c++
// Pseudocode
void Graph::dijkstra(Vertex s) {
  for each Vertex v {
    v.dist = INFINITY;
    v.known = false;
  }
  s.dist = 0;
  while (there is an unknown distance vertex) {
    Vertex v = smallest unknown distance vertex;
    
    v.known = true;
    
    for each Vertex w adjacent to v
      if (!w.known) {
        DistType cvw = cost of edge from v to w;
        
        if ((v.dist + cvw) < w.dist) {
          // Update w
          decrease(w.dist to v.dist + cvw);
          w.path = v;
        }
      }
  }
}
```

If using a priority queue to choose unknown distance vertex, the running time is O(\|E\|log\|V\|).

#### Remarks

- Dijkstra's algorithm is an example of a **greedy algorithm**.