# Shortest Path Finder in an Undirected Graph using BFS

This program finds the shortest path between a source and a destination node in an undirected graph using the Breadth-First Search (BFS) algorithm.

## Overview

- **Input**: Number of vertices, edges, edge connections, source node, and terminal node.
- **Output**: The shortest path from the source node to the terminal node.

## Features

- Constructs an adjacency list representation of the graph.
- Utilizes BFS to traverse the graph and find the shortest path.
- Handles undirected graphs effectively.

## Requirements

- C++11 or higher
- Standard library (`<bits/stdc++.h>`)

## How It Works

1. **Input**:
   - Users provide the number of vertices and edges.
   - Users specify the edges between vertices.
   - Users input the source and terminal nodes.

2. **Graph Representation**:
   - The graph is represented using an adjacency list stored in an `unordered_map`.

3. **BFS Traversal**:
   - A queue is used to facilitate BFS.
   - The algorithm tracks visited nodes and their parents to reconstruct the path later.

4. **Path Reconstruction**:
   - Once the terminal node is reached, the path is reconstructed by following parent pointers from the terminal to the source.

5. **Output**:
   - The program prints the shortest path from the source to the terminal.

## Example Usage

### Sample Input/Output

#### Input

```
Enter the number of vertex: 5
Enter the number of edgeCount: 6
Enter edge (u v):
0 1
0 2
1 3
1 4
2 4
3 4
Enter the source node: 0
Enter the terminal: 4
```

#### Output

```
Shortest path from 0 to 4: 0 1 4 
```

### Explanation of the Example

**Graph Representation:**

Given the edges, the undirected graph can be represented as follows:

```
      0
     / \
    1   2
   / \   \
  3   4---+
```

**Steps to Find the Shortest Path from Node 0 to Node 4:**

1. Start at the source node **0**. 
2. The neighbors of **0** are **1** and **2**.
3. Move to **1** (queue becomes [1, 2]).
4. From **1**, the neighbors are **0**, **3**, and **4**. 
5. Visit **4** (queue becomes [2, 3, 4]), and note that the parent of **4** is **1**.
6. The shortest path is then reconstructed by backtracking from **4** to **1** to **0**.

The shortest path found is **0 → 1 → 4**.

## Important Information

- **BFS Complexity**: The time complexity of the BFS algorithm is O(V + E), where V is the number of vertices and E is the number of edges. This makes BFS efficient for sparse graphs.
  
- **Path Validity**: The program assumes a valid path exists between the source and the terminal nodes. If no path exists, the output may not represent a valid route.

- **Graph Characteristics**: The graph must be undirected and can have multiple edges or nodes. The BFS approach guarantees that the shortest path is found in an unweighted graph.

## Graph Visualization

![Graph Visualization](https://via.placeholder.com/400x300.png?text=Graph+Visualization)

*(Note: Replace with an actual graph image for better clarity.)*
