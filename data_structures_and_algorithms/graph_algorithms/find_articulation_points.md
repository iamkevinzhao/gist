## Find Articulation Points

- [Upper Level](README.md)

#### Definition

- Biconnected

> A connected undirected graph is biconnected if there are no vertices whose removal disconnects the rest of the graph.

- Articulation Points

> If a graph is not biconnected, articulation points are the vertices whose removal would disconnect the graph.

```c++
// Pseudocode
void Graph::findArt(Vertex v) {
  v.visited = true;
  v.low = v.num = counter++;
  for each Vertex w adjacent to v {
    if (!w.visited) {
      w.parent = v;
      findArt(w);
      if (w.low >= v.num)
        cout << v << " is an articulation point" << endl;
      v.low = min(v.low, w.low);
    } else if (v.parent != w)
      v.low = min(v.low, w.num);
  }
}
```

Refer to "Data Structures and Algorithm Analysis Edition 4" by Mark Allen Weiss, Chapter 9.6.2 Biconnectivity.