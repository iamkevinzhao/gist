## Dijkstra's Algorithm

- [Upper Level](README.md)

Dijkstra's algorithm is for solving the weighted shortest path problem.

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

