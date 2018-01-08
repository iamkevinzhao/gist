## Topological Sort

#### Definition

> A topological sort is an ordering of vertices in a directed acyclic graph, such that if there is a path from vertex i to vertex j, then vertex j appears after vertex i in the ordering.

#### Applications

- College course prerequisite structure
- Software package dependencies

#### A Simple Approach (Takes O(|v|<sup>2</sup>) Time)

```c++
// Pseudocode
void Graph::topsort() {
  for (int counter = 0; counter < NUM_VERTICES; ++counter) {
    Vertex v = findNewVertexofIndgreeZero();
    if (v == NOT_A_VERTEX)
      throw CycleFoundException{};
    v.topNum = counter;
    for each Vertex w adjacent to v
      --w.indegree;
  }
}
```

#### An Efficient Approach (Takes O(|E|+|V|) Time)

```c++
// Pseudocode
void Graph::topsort() {
  Queue<Vertex> q;
  int counter = 0;
  
  q.makeEmpty();
  for each Vertex v
    if (v.indegree == 0)
      q.enqueue(v);
  while (!q.isEmpty()) {
    Vertex v = q.dequeue();
    v.topNum = ++counter;
    
    for each Vertex w adjacent to v
      if (--w.indegree == 0)
        q.enqueue(w);
  }
  if (counter != NUM_VERTICES)
    throw CycleFoundException{};
}
```

---

**indegree**: 

> The indegree of a vertex v is the number of edges (u, v) in a graph.