# Cycle Detection in Undirected Graph Using DFS

This repository contains a C++ program that detects cycles in an undirected graph using the Depth-First Search (DFS) algorithm. 

## Overview

The program creates an adjacency list representation of the graph from user-input edges and utilizes DFS to check for cycles. It can handle both connected and disconnected graphs.

## Features

- Input for the number of vertices and edges.
- Input for each edge in the form of two vertices (u, v).
- Detects cycles in the graph and outputs whether a cycle exists.

## Getting Started

### Prerequisites

Make sure you have a C++ compiler installed. You can use g++ for compiling the code.

### Compilation

To compile the program, use the following command:

```bash
g++ cycle_detection.cpp -o cycle_detection
```

### Usage

Run the compiled program:

```bash
./cycle_detection
```

### Input

The program will prompt for the following inputs:

1. Number of vertices in the graph.
2. Number of edges.
3. Edges in the form of pairs (u v), where u and v are vertices connected by an edge.

## Example

### Input

```
Enter the number of vertex: 5
Enter the number of edgeCount: 5
Enter edge (u v):
0 1
1 2
2 0
1 3
3 4
```

### Explanation

1. **Graph Representation**: The input represents the following undirected graph:

   ```
      0
     / \
    1---2
    |
    3
    |
    4
   ```

   - Vertices: 0, 1, 2, 3, 4
   - Edges: (0, 1), (1, 2), (2, 0) - forms a cycle; (1, 3), (3, 4) - no cycle.

2. **Cycle Detection Process**:
   - Starting from vertex 0:
     - Visit 0 → mark as visited.
     - Move to neighbor 1.
   - From 1:
     - Visit 1 → mark as visited.
     - Move to neighbor 2.
   - From 2:
     - Visit 2 → mark as visited.
     - Move to neighbor 0, which is already visited (but not the parent of 2), indicating a cycle.
  
3. **Output**: 
   - The program outputs: `Cycle is present: YES`.

## Important Points

- **Adjacency List**: An efficient way to represent sparse graphs. It allows easy traversal and memory efficiency.
  
- **DFS Approach**: 
  - Depth-First Search is ideal for exploring all paths in a graph.
  - The algorithm checks if a visited vertex is not the parent of the current vertex to detect cycles.

- **Handling Disconnected Graphs**: 
  - The program iterates through all vertices, ensuring that it checks each component of the graph.

- **Complexity**:
  - Time Complexity: \(O(V + E)\), where \(V\) is the number of vertices and \(E\) is the number of edges.
  - Space Complexity: \(O(V)\) for the visited list and the adjacency list.

## Code Explanation

1. **Adjacency List Creation**: The program builds an adjacency list from the input edges.

2. **DFS for Cycle Detection**: A recursive DFS function checks each vertex's neighbors. If a visited neighbor is found that is not the parent of the current vertex, a cycle is detected.

3. **Handling Disconnected Graphs**: The program iterates through all vertices to ensure all components are checked.

## Functions

- `bool dfsConceptForCycleDetection(...)`: Helper function that performs DFS and checks for cycles.
  
- `string cycleDetectionInUndirectedGraph(...)`: Main function to create the adjacency list and initiate DFS for cycle detection.
 

## Acknowledgments

- Inspired by algorithms and data structures for graph theory.
