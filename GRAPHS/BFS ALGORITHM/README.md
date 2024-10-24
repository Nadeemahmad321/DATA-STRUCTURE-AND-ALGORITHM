# Breadth First Search (BFS) Implementation

This program implements the Breadth First Search (BFS) algorithm for traversing or searching through a graph. The graph is represented using an adjacency list. The BFS algorithm explores all the neighboring nodes at the present depth prior to moving on to nodes at the next depth level.

## Features

- Handles both directed and undirected graphs.
- Supports disconnected graphs by checking all vertices.
- Uses a queue to manage the nodes to be explored.

## Graph Representation

The graph is represented using an adjacency list, which is a map where each key is a vertex and the associated value is a list of neighboring vertices. This structure allows for efficient traversal.

### Example Graph

Consider the following undirected graph:

```
    0
   / \
  1   2
 / \
3   4
```

### Edges Representation

- Vertices: 5 (0, 1, 2, 3, 4)
- Edges:
  - (0, 1)
  - (0, 2)
  - (1, 3)
  - (1, 4)

This can be represented as:
```
0: [1, 2]
1: [0, 3, 4]
2: [0]
3: [1]
4: [1]
```

## How to Run

### Prerequisites

- C++ compiler (g++, clang++, etc.)

### Steps

1. **Clone or Download the Repository**:
   ```bash
   git clone <repository_url>
   cd <repository_directory>
   ```

2. **Compile the Code**:
   ```bash
   g++ -o bfs bfs.cpp
   ```

3. **Run the Executable**:
   ```bash
   ./bfs
   ```

### Input Format

- The program first prompts for the number of vertices in the graph.
- Then, it asks for the number of edges.
- Finally, it requires the edges as pairs of integers (u, v), where `u` and `v` are the vertices connected by the edge.

### Example Input

```
Enter the number of vertex: 5
Enter the number of edgeCount: 4
Enter the edges (u v) pairs:
0 1
0 2
1 3
1 4
```

### Example Output

```
Breadth first search: 0 1 2 3 4
```

## Explanation of Output

1. **Starting Node**: The BFS begins at node `0`.
2. **Exploration**:
   - Node `0` is visited first and added to the result.
   - From `0`, we explore its neighbors: `1` and `2`. Both are added to the queue.
   - Next, `1` is dequeued, visited, and its neighbors (`0`, `3`, `4`) are explored. Nodes `3` and `4` are added to the queue.
   - Then, `2` is dequeued and visited. It has no unvisited neighbors.
   - Finally, `3` and `4` are dequeued and visited in that order.

3. **Final Order**: The BFS traversal order is `0, 1, 2, 3, 4`, which is printed as the result.

## Code Explanation

### Key Components

- **BFS Function**:
  - Uses a queue to explore nodes layer by layer.
  - Marks nodes as visited to avoid processing the same node multiple times.
  
- **Adjacency List**:
  - Created from the input edges, allowing efficient traversal of neighbors.

- **Main Function**:
  - Handles user input and initiates the BFS algorithm.

## Complexity Analysis

- **Time Complexity**: O(V + E), where V is the number of vertices and E is the number of edges.
- **Space Complexity**: O(V), primarily for the queue and adjacency list.
