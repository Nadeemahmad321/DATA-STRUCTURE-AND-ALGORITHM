# Cycle Detection in Directed Graph Using DFS

This program detects cycles in a directed graph using Depth First Search (DFS). It takes the number of vertices and edges as input, along with the edges themselves, and determines if there is a cycle present in the graph.

## Table of Contents
- [Features](#features)
- [How It Works](#how-it-works)
- [Graph Representation](#graph-representation)
- [Input Format](#input-format)
- [Output Format](#output-format)
- [Usage](#usage)
- [Example](#example)
- [Important Information](#important-information)
- [Requirements](#requirements)

## Features
- Uses Depth First Search for cycle detection.
- Handles both connected and disconnected graphs.
- User-friendly input and output.

## How It Works
1. **Graph Representation**: The graph is represented using an adjacency list.
2. **DFS Traversal**: The program uses a recursive DFS function to traverse the graph.
3. **Cycle Detection**: It keeps track of visited nodes and nodes in the current DFS path to detect cycles. If a node is revisited while it's still in the current DFS path, a cycle exists.

## Graph Representation
In a directed graph, edges have a direction, meaning they point from one vertex to another. The adjacency list is a common way to represent such graphs. Each vertex points to a list of its adjacent vertices (i.e., vertices it directs to).

### Example Graph
Consider the following directed graph:

```
    0 → 1
    ↑   ↓
    2 ← 3
```

This graph can be represented by the following edges:
- (0, 1)
- (1, 3)
- (3, 2)
- (2, 0)

In this graph, there is a cycle involving the vertices 0, 1, 2, and 3.

## Input Format
- First, enter the number of vertices in the graph.
- Next, enter the number of edges.
- Finally, for each edge, provide two integers representing the directed edge from vertex `u` to vertex `v`.

### Example Input
```
Enter the number of vertex: 4
Enter the number of edgeCount: 4
Enter edge (u v):
0 1
1 2
2 0
3 3
```

## Output Format
The program will output whether a cycle is present in the directed graph.

### Example Output
```
Cycle is present.
```

## Usage
1. Compile the code using a C++ compiler.
2. Run the executable and provide the input in the specified format.
3. Observe the output indicating the presence of a cycle.

## Example
### Input
```
Enter the number of vertex: 4
Enter the number of edgeCount: 5
Enter edge (u v):
0 1
1 2
2 0
3 1
3 2
```

### Explanation
- **Input Breakdown**:
  - The graph has 4 vertices (0, 1, 2, 3).
  - It has 5 directed edges:
    - From vertex 0 to vertex 1
    - From vertex 1 to vertex 2
    - From vertex 2 to vertex 0 (this creates a cycle)
    - From vertex 3 to vertex 1
    - From vertex 3 to vertex 2

- **DFS Traversal**:
  1. Start at vertex 0: mark it as visited and in the current path.
  2. Move to vertex 1: mark it as visited and in the current path.
  3. Move to vertex 2: mark it as visited and in the current path.
  4. Move back to vertex 0 (already in the current path), indicating a cycle.

### Output
```
Cycle is present.
```

### Alternative Input
```
Enter the number of vertex: 3
Enter the number of edgeCount: 2
Enter edge (u v):
0 1
1 2
```

### Explanation
- **Input Breakdown**:
  - The graph has 3 vertices (0, 1, 2).
  - It has 2 directed edges:
    - From vertex 0 to vertex 1
    - From vertex 1 to vertex 2
- **DFS Traversal**:
  - Start at vertex 0, then move to vertex 1, then to vertex 2. No backtracking to an already visited node occurs, so no cycle is detected.

### Output
```
Cycle is not present.
```

## Important Information
- **Time Complexity**: The time complexity of this cycle detection algorithm is \(O(V + E)\), where \(V\) is the number of vertices and \(E\) is the number of edges. This is efficient for sparse graphs.
- **Space Complexity**: The space complexity is \(O(V)\) due to the storage used for the adjacency list and the visited arrays.
- **Directed vs. Undirected**: This method is specific to directed graphs. Cycle detection in undirected graphs has a different approach and considerations.

## Requirements
- C++11 or higher for compiling.
- Standard input/output.

This program provides a straightforward implementation of cycle detection in directed graphs using DFS, making it suitable for educational purposes and basic algorithm understanding.
