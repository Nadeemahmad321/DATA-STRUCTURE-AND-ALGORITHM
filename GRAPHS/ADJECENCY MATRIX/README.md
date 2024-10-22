# Graph Adjacency Matrix

This C++ program creates an adjacency matrix representation of a graph. It allows users to input the number of vertices and edges, and then it generates and displays the corresponding adjacency matrix.

## Table of Contents

- [Features](#features)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Code Explanation](#code-explanation)
- [Example](#example)

## Features

- Input for the number of vertices and edges.
- Interactive edge input for undirected graphs.
- Output of the adjacency matrix.

## Getting Started

### Prerequisites

- C++ Compiler (e.g., g++, clang++)
- Standard Library (C++11 or later)

### Compilation

To compile the program, use the following command:

```bash
g++ -o adjacency_matrix adjacency_matrix.cpp
```

### Execution

Run the program using the command:

```bash
./adjacency_matrix
```

## Usage

1. When prompted, enter the number of vertices in the graph.
2. Enter the number of edges.
3. For each edge, input two vertex indices (u and v) to represent an undirected edge between them.
4. The program will output the adjacency matrix of the graph.

## Code Explanation

- **Headers**: Includes necessary headers for input/output and vector manipulation.
- **addEdge Function**: A utility function to add edges between two vertices in the adjacency matrix.
- **Main Function**:
  - Initializes the adjacency matrix with zeros.
  - Accepts user input for the number of vertices and edges.
  - Collects edges and updates the adjacency matrix.
  - Prints the final adjacency matrix.

### Key Functions

- `addEdge(int u, int v, vector<vector<int>>& adjMatrix)`: Updates the adjacency matrix for the edge between vertices `u` and `v`.

## Example

```
Enter the number of vertex: 4
Enter the number of edges: 4
Enter edge (u v):
0 1
0 2
1 2
2 3

Adjacency matrix is:
0 1 1 0 
1 0 1 0 
1 1 0 1 
0 0 1 0 
```

This output shows an undirected graph with vertices 0, 1, 2, and 3, where edges exist between specified pairs.
