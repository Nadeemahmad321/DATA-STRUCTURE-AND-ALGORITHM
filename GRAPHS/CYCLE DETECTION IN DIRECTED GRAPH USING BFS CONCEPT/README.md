# Cycle Detection in Directed Graph Using BFS

This program implements cycle detection in a directed graph using the BFS (Breadth-First Search) concept. It leverages the idea of tracking in-degrees of vertices to determine if a cycle exists in the graph.

## Table of Contents
- [Overview](#overview)
- [How It Works](#how-it-works)
- [Usage](#usage)
- [Example](#example)
- [Code Explanation](#code-explanation)
- [Input Format](#input-format)
- [Output Format](#output-format)
- [Important Information](#important-information)
- [Dependencies](#dependencies)

## Overview

Cycle detection is crucial in many applications, such as deadlock detection in operating systems, verifying the correctness of algorithms, and ensuring the integrity of data structures. This program identifies whether a directed graph contains a cycle.

## How It Works

1. **Adjacency List Creation**: The program constructs an adjacency list from the input edges.
2. **In-degree Calculation**: It calculates the in-degree (number of incoming edges) for each vertex.
3. **BFS Traversal**: Using a queue, it performs a BFS traversal starting from all vertices with zero in-degree.
4. **Cycle Detection**: If the number of visited vertices equals the total number of vertices, there is no cycle; otherwise, a cycle exists.

## Usage

To run the program, follow these steps:

1. Compile the code using a C++ compiler.
2. Execute the binary.
3. Enter the number of vertices and edges, followed by the edge pairs.

## Example

### Graph Representation

Consider the following directed graph:

```
   (0) → (1)
    ↑    |
    |    ↓
   (3) ← (2)
```

### Edge List

- Vertex Count: 4
- Edges:
  - 0 → 1
  - 1 → 2
  - 2 → 3
  - 3 → 1 (This edge creates a cycle)

### Input Example

```
Enter the number of vertices: 4
Enter the number of edges: 4
Enter edge (u v):
0 1
1 2
2 3
3 1
```

### Expected Output

```
Cycle is present.
```

### Explanation

1. **Adjacency List Creation**:
   - From the edges, the adjacency list will be:
     - 0 → [1]
     - 1 → [2]
     - 2 → [3]
     - 3 → [1]

2. **In-degree Calculation**:
   - Vertex 0: in-degree = 0
   - Vertex 1: in-degree = 2 (from 0 and 3)
   - Vertex 2: in-degree = 1 (from 1)
   - Vertex 3: in-degree = 1 (from 2)

3. **BFS Traversal**:
   - Start with vertices that have an in-degree of 0. Here, only vertex 0 qualifies.
   - Process vertex 0 → Queue becomes [1].
   - Process vertex 1 → Queue becomes [2].
   - Process vertex 2 → Queue becomes [3].
   - Process vertex 3 → Notice that vertex 1 is now reachable again, indicating a cycle.

4. **Cycle Detection**: Since not all vertices were visited (only 4 out of 4 were reachable), a cycle is confirmed.

## Code Explanation

### Main Components

- **Function**: `cycleDetectionInDirectedGraph(int vertex, vector<vector<int>>& edges)`
  - Constructs the adjacency list and calculates in-degrees.
  - Performs BFS to detect cycles.
  
- **Input Handling**: Reads the number of vertices and edges, then the edges themselves.

### Example Code Snippet
```cpp
#include<bits/stdc++.h>
using namespace std;

bool cycleDetectionInDirectedGraph(int vertex, vector<vector<int>>& edges) {
    // Implementation...
}

int main() {
    // Input handling...
}
```

## Input Format

- The first input line contains two integers:
  - `vertex`: Total number of vertices in the graph.
  - `edgeCount`: Total number of edges in the graph.
- The next `edgeCount` lines each contain two integers `u` and `v`, representing a directed edge from vertex `u` to vertex `v`.

## Output Format

- The program outputs:
  - "Cycle is present." if a cycle exists in the directed graph.
  - "Cycle is not present." if no cycle is found.

## Important Information

- **Complexity**: The time complexity of this algorithm is O(V + E), where V is the number of vertices and E is the number of edges. This is efficient for cycle detection.
- **Graph Properties**: A directed graph may have multiple cycles, but this algorithm checks for the presence of at least one.
- **Applications**: This approach can be used in scenarios such as dependency resolution, task scheduling, and various graph algorithms.

## Dependencies

- C++ Standard Library
