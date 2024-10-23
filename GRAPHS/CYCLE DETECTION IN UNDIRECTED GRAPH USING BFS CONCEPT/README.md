# Cycle Detection in Undirected Graph Using BFS

This program implements cycle detection in an undirected graph using the Breadth-First Search (BFS) algorithm. It allows users to input the number of vertices and edges, followed by the edges themselves, and then checks if a cycle exists in the graph.

## Features
- Detects cycles in undirected graphs.
- Utilizes BFS for traversal.
- Handles disconnected graphs.

## How It Works
1. **Input**: The user provides the number of vertices and edges, followed by pairs of vertices representing the edges.
2. **Adjacency List Creation**: An adjacency list is constructed to represent the graph.
3. **BFS Traversal**: The BFS algorithm is used to explore the graph. A parent mapping is maintained to distinguish between a back edge and a simple traversal.
4. **Cycle Detection**: If a visited node is encountered that is not the parent of the current node, a cycle is detected.

## Code Overview

### Functions
- **`bfsConceptForCycleDetection`**: Implements the BFS logic to check for cycles.
- **`cycleDetectionInUndirectedGraph`**: Orchestrates the cycle detection process and handles the creation of the adjacency list.

### Main Function
- Takes user input for vertices and edges.
- Calls the cycle detection function and prints whether a cycle is present.

## Example Input/Output
### Input:
```
Enter the number of vertex: 5
Enter the number of edgeCount: 5
Enter edge (u v):
0 1
1 2
2 0
0 3
3 4
```

### Output:
```
Cycle is present: YES
```

### Explanation
The provided edges form the following graph:

```
    0
   / \
  1---2
  |
  3
  |
  4
```

- **Vertices**: 0, 1, 2, 3, 4
- **Edges**:
  - 0 connects to 1 and 2
  - 1 connects to 2 (forming a cycle: 0 → 1 → 2 → 0)
  - 0 connects to 3
  - 3 connects to 4

### Cycle Detection Process:
1. Start BFS from vertex 0.
2. Mark 0 as visited. Parent of 0 is -1.
3. Visit neighbors of 0: 
   - Visit 1, mark as visited, parent of 1 is 0.
   - Visit 2, mark as visited, parent of 2 is 0.
4. From 1, visit its neighbors:
   - 0 is already visited (parent), skip.
   - Visit 2 (already visited, but it's not the parent of 1), indicating a cycle.
5. The function returns "YES" indicating a cycle is present.

## Graph Representation
You can visualize the graph with vertices and edges as follows:

```plaintext
    0
   / \
  1---2
  |
  3
  |
  4
```

## Requirements
- C++ Standard Library (for `bits/stdc++.h`, `unordered_map`, `list`, and `queue`)

## Compilation and Execution
To compile and run the program, use the following commands in a terminal:

```bash
g++ cycle_detection.cpp -o cycle_detection
./cycle_detection
```

## Notes
- Ensure that you provide a valid number of vertices and edges.
- The program assumes vertices are labeled from `0` to `vertex - 1`.
