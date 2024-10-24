# Dijkstra's Algorithm Implementation

This repository contains a C++ implementation of Dijkstra's algorithm, which finds the shortest paths from a source node to all other nodes in a weighted graph. The graph is represented as an adjacency list, and the implementation handles undirected graphs.

## Description

Dijkstra's algorithm is efficient for graphs with non-negative weights and is widely used in routing and navigation applications. It works by maintaining a set of nodes whose shortest distance from the source is known, and iteratively expanding this set.

### Key Features
- Input graph defined by edges with weights
- Supports multiple nodes and edges
- Outputs shortest distances from a specified source node

## Requirements
- C++ Compiler (C++11 or higher recommended)
- Standard Template Library (STL) support

## How to Compile and Run

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. **Compile the program:**
   ```bash
   g++ -o dijkstra dijkstra.cpp
   ```

3. **Run the program:**
   ```bash
   ./dijkstra
   ```

## Input Format
The program prompts for:
1. Number of vertices
2. Number of edges
3. Edge list (u, v, w) where `u` and `v` are nodes and `w` is the weight of the edge connecting them
4. The source node from which to calculate shortest paths

### Example Input
```
Enter the number of vertex: 5
Enter the number of edgeCount: 6
Enter edges (u v w):
0 1 10
0 2 3
1 2 1
1 3 2
2 1 4
2 3 8
2 4 2
4 3 7
Enter the source: 0
```

## Example Output
```
Shortest paths from node 0:
Node 0: 0
Node 1: 7
Node 2: 3
Node 3: 9
Node 4: 5
```

## Visual Representation of the Graph

Here's a visual representation of the example graph:

```
      (10)
  0 --------- 1
   | \        | \
(3)|  \ (1)  |  \(2)
   |   \     |   \
   |    \    |    \
   2 --------- 3
   | \       / \
(2)|  \(8) /   \(7)
   |   \   /     \
   4 ----------- 
```

### Explanation of the Example

1. **Graph Construction:**
   - The graph has 5 vertices (0, 1, 2, 3, 4) and the following edges with weights:
     - (0, 1) with weight 10
     - (0, 2) with weight 3
     - (1, 2) with weight 1
     - (1, 3) with weight 2
     - (2, 1) with weight 4
     - (2, 3) with weight 8
     - (2, 4) with weight 2
     - (4, 3) with weight 7

2. **Running the Algorithm:**
   - Starting from node 0, the algorithm initializes the distances: 
     - Distance to node 0 = 0 (source)
     - Distance to all other nodes = ∞
   - The initial distances are: `[0, ∞, ∞, ∞, ∞]`

3. **Iterations:**
   - **Iteration 1:** 
     - Visit node 0, update neighbors:
       - Distance to 1: `0 + 10 = 10`
       - Distance to 2: `0 + 3 = 3`
     - Updated distances: `[0, 10, 3, ∞, ∞]`
   - **Iteration 2:**
     - Visit node 2 (smallest distance), update neighbors:
       - Distance to 1: `3 + 1 = 4` (update from 10 to 4)
       - Distance to 3: `3 + 8 = 11` (temporary)
       - Distance to 4: `3 + 2 = 5`
     - Updated distances: `[0, 4, 3, 11, 5]`
   - **Iteration 3:**
     - Visit node 1, update neighbors:
       - Distance to 3: `4 + 2 = 6` (update from 11 to 6)
     - Updated distances: `[0, 4, 3, 6, 5]`
   - **Iteration 4:**
     - Visit node 4, no updates (distances remain)
   - **Iteration 5:**
     - Visit node 3, no updates (distances remain)

4. **Final Distances:**
   - The final distances from node 0 to all nodes are:
     - Node 0: 0
     - Node 1: 4
     - Node 2: 3
     - Node 3: 6
     - Node 4: 5

## Important Information
- Dijkstra's algorithm does not work with negative weight edges. If the graph contains such edges, consider using the Bellman-Ford algorithm instead.
- The time complexity of Dijkstra's algorithm is \(O((V + E) \log V)\) where \(V\) is the number of vertices and \(E\) is the number of edges, especially when using a priority queue.
