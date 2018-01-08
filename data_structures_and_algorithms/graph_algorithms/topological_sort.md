## Topological Sort

#### Definition

> A topological sort is an ordering of vertices in a directed acyclic graph, such that if there is a path from vertex i to vertex j, then vertex j appears after vertex i in the ordering.

#### Applications

- College course prerequisite structure
- Software package dependencies

#### A Naive Approach (Takes O(|v|<sup>2</sup>) Time)

```c++
// Pseudocode
void Graph::topsort() {
  for (int counter = 0; counter < NUM_VERTICES; ++counter) {
    Vertex v = findNewVertexofIndgreeZero();
  }
}
```

