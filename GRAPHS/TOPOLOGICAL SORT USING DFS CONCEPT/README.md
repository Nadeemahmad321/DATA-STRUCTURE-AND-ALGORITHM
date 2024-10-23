# Topological Sort using DFS

This program implements topological sorting of a directed acyclic graph (DAG) using Depth First Search (DFS). Topological sorting provides a linear ordering of vertices such that for every directed edge `u -> v`, vertex `u` comes before vertex `v`.

## Features

- Implements topological sort using DFS.
- Works with directed acyclic graphs (DAGs).
- Handles disconnected graphs.

## Important Information

- **Directed Acyclic Graph (DAG)**: A directed graph with no cycles. Topological sorting is only applicable to DAGs.
- **Linear Ordering**: The result is not necessarily unique; multiple valid topological sorts may exist for a single graph.
- **Complexity**: The algorithm runs in O(V + E) time, where V is the number of vertices and E is the number of edges.

## Requirements

- C++11 or later.

## Compilation

To compile the program, use a C++ compiler such as g++. For example:

```bash
g++ -o topological_sort topological_sort.cpp
```

## Usage

1. Run the compiled program:

   ```bash
   ./topological_sort
   ```

2. Input the number of vertices and edges:

   ```
   Enter the number of vertex: [number_of_vertices]
   Enter the number of edgeCount: [number_of_edges]
   ```

3. Enter the edges in the format `u v`:

   ```
   Enter edge (u v):
   [edge_1]
   [edge_2]
   ...
   ```

4. The program will output the topological sort of the graph:

   ```
   Topological sort is: [sorted_vertices]
   ```

## Example

### Graph Representation

Consider the following directed acyclic graph (DAG):

```
     0
    / \
   1   2
    \ /
     3
```

### Edge List Representation

This graph can be represented with the following edges:

- `0 -> 1`
- `0 -> 2`
- `1 -> 3`
- `2 -> 3`

### Input Example

Given the above graph:

```
Enter the number of vertex: 4
Enter the number of edgeCount: 4
Enter edge (u v):
0 1
0 2
1 3
2 3
```

### Output

The output will be a valid topological sort of the graph:

```
Topological sort is: 0 1 2 3
```

### Explanation

1. **Input Handling**:
   - The program prompts for the number of vertices and edges and then reads the edges.
   
2. **Graph Construction**:
   - An adjacency list is created to represent the graph, where each node points to its directed neighbors.
   
3. **DFS Traversal**:
   - The `topoSort` function is called recursively to perform a depth-first search. Nodes are marked as visited, and once all neighbors of a node are processed, the node is pushed onto a stack.

4. **Final Order**:
   - Once all nodes have been processed, nodes are popped from the stack to produce the topological order. The result is a valid linear ordering that respects the direction of edges.

## Code Explanation

### Functions

- **`topoSort`**:
  - A recursive function that marks the current node as visited and explores its unvisited neighbors. When all neighbors are processed, it pushes the node onto a stack.

- **`topoLogicalSort`**:
  - Initializes the adjacency list, handles visited nodes, and ensures that all nodes (including those in disconnected components) are processed.

### Main Function

The `main` function manages user input for vertices and edges, constructs the graph, and calls the `topoLogicalSort` function to retrieve the topological order.

## Visual Representation

Here is a visual representation of the graph used in the example:

```
     0
    / \
   1   2
    \ /
     3
```

- **Vertex 0** is the starting point and directs edges to vertices **1** and **2**.
- Both **1** and **2** direct edges to vertex **3**, ensuring that **3** comes after both in the topological sort.

## Conclusion

This implementation of topological sort provides a simple yet effective way to order vertices in a directed acyclic graph. The use of DFS ensures that we explore all possible paths while maintaining the necessary order dictated by the edges.
