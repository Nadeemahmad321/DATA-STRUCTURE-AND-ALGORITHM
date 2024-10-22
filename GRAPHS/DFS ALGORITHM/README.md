# Depth First Search (DFS) Algorithm

## Description
This program implements the Depth First Search (DFS) algorithm to explore a graph. It constructs an adjacency list from user-input edges and performs DFS to find all connected components in the graph.

## Features
- Handles both directed and undirected graphs.
- Can find multiple connected components in a disconnected graph.
- Utilizes a recursive approach for the DFS traversal.

## How It Works
1. **Input**: The user provides the number of vertices and edges, followed by the edge pairs that define the graph.
2. **Adjacency List Construction**: The program builds an adjacency list to represent the graph.
3. **DFS Traversal**: The program visits each vertex, marking it as visited, and recursively explores its unvisited neighbors.
4. **Output**: The program prints the connected components found during the DFS.

## Example
Let’s consider an example to illustrate how the DFS algorithm works.

### Input
```
Number of vertices: 5
Number of edges: 4
Edges (u v):
0 1
0 2
1 2
3 4
```

### Explanation
1. **Graph Representation**:
   - The input specifies 5 vertices (0 to 4) and 4 edges:
     - Edge between 0 and 1
     - Edge between 0 and 2
     - Edge between 1 and 2
     - Edge between 3 and 4
   - The adjacency list representation of this graph will look like:
     ```
     0: [1, 2]
     1: [0, 2]
     2: [0, 1]
     3: [4]
     4: [3]
     ```

2. **Depth First Search Process**:
   - The algorithm starts at vertex 0.
   - It visits 0, marking it as visited, and adds it to the current component.
   - It then explores the neighbors of 0, starting with 1.
     - From 1, it visits its unvisited neighbor, which is 2, marking it as visited.
     - Since 2 has no unvisited neighbors, the traversal for this component ends.
   - The first connected component found is `[0, 1, 2]`.

3. **Continuing the Search**:
   - The algorithm then checks vertex 1 and 2, but both are already visited.
   - It moves to vertex 3, which is unvisited. It marks 3 as visited and starts a new component.
   - The only neighbor of 3 is 4, which is also unvisited. It visits 4 and completes the second component.
   - The second connected component found is `[3, 4]`.

### Output
The final output displays the connected components:
```
Depth First Search components are:
0 1 2 
3 4 
```

## Instructions to Compile and Run
1. Ensure you have a C++ compiler installed (like g++).
2. Save the code in a file named `dfs.cpp`.
3. Open a terminal and navigate to the directory containing the file.
4. Compile the code using:
   ```bash
   g++ -o dfs dfs.cpp
   ```
5. Run the compiled program:
   ```bash
   ./dfs
   ```

## Notes
- The algorithm uses an adjacency list representation for efficient traversal.
- The program handles cases where the graph may be disconnected, identifying all components.
