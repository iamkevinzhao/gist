## Heapsort

- [Upper Level](README.md)

Refer to "Introduction to Algorithms, 3rd Edition", Chapter 6, "Heapsort"

#### Procedures

- Max Heapify
  - O(lgn)
- Build Max Heap
  - O(n)
- Heapsort
  - O(nlgn)
- Max Heap Insert
  - O(lgn)
- Heap Extract Max
  - O(lgn)
- Heap Increase Key
  - O(lgn)
- Heap Maximum 
  - O(lgn)

#### Max Heapify

> "Float down" a heap node so that the subtree rooted at the node obeys that max-heap property.

- Max-Heap Property:

  > For every node i other than the root, A[Parent(i)] >= A[i], while A is the heap.

#### Build a Heap

Convert an array into a max-heap.