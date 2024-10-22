# Graph Representation using Adjacency List

This program demonstrates how to represent a graph using an adjacency list in C++. It allows users to input the number of vertices and edges, and then define the edges of the graph. The program constructs the adjacency list and displays it.

## Features

- Input the number of vertices and edges.
- Define edges as pairs of vertices (u, v).
- Construct and display the adjacency list for the graph.

## How to Use

1. **Compile the Program**: Use a C++ compiler to compile the code. For example, using g++:
   ```bash
   g++ graph_representation.cpp -o graph_representation
   ```

2. **Run the Program**:
   ```bash
   ./graph_representation
   ```

3. **Input**:
   - Enter the number of vertices.
   - Enter the number of edges.
   - For each edge, enter two integers (u, v) representing an edge between vertex u and vertex v.

4. **Output**: The program will output the adjacency list of the graph.

## Example

### Input
```
Enter the number of vertex: 4
Enter the number of edgeCount: 5
Enter edge (u v):
0 1
0 2
1 2
1 3
2 3
```

### Output
```
Adjacency List is:
0->1 2 
1->0 2 3 
2->0 1 3 
3->1 2 
```

### Explanation
- **Vertices**: There are 4 vertices labeled `0`, `1`, `2`, and `3`.
- **Edges**: 
  - An edge between `0` and `1` connects vertex `0` to vertex `1`.
  - An edge between `0` and `2` connects vertex `0` to vertex `2`.
  - An edge between `1` and `2` connects vertex `1` to vertex `2`.
  - An edge between `1` and `3` connects vertex `1` to vertex `3`.
  - An edge between `2` and `3` connects vertex `2` to vertex `3`.

### Adjacency List Explanation
- The adjacency list for each vertex shows which vertices are directly connected:
  - **Vertex `0`**: Connected to `1` and `2`.
  - **Vertex `1`**: Connected to `0`, `2`, and `3`.
  - **Vertex `2`**: Connected to `0`, `1`, and `3`.
  - **Vertex `3`**: Connected to `1` and `2`.

## Code Explanation

- The program uses the STL `map` and `list` to create the adjacency list.
- The `addEdge` function populates the adjacency list based on the edges provided:
  ```cpp
  map<int,list<int>> addEdge(int vertex, vector<vector<int>>& edges) {
      map<int, list<int>> adjList;
      for(int i = 0; i < edges.size(); i++) {
          int u = edges[i][0];
          int v = edges[i][1];
          adjList[u].push_back(v); // Add edge from u to v
          adjList[v].push_back(u); // Add edge from v to u (for undirected graph)
      }
      return adjList;
  }
  ```
- The `main` function handles user input and outputs the adjacency list:
  ```cpp
  int main() {
      int vertex, edgeCount;
      cout << "Enter the number of vertex:";
      cin >> vertex;
      cout << "Enter the number of edgeCount:";
      cin >> edgeCount;

      vector<vector<int>> edges(edgeCount, vector<int>(2));
      cout << "Enter edge (u v):" << endl;
      for(int i = 0; i < edgeCount; i++) {
          cin >> edges[i][0] >> edges[i][1];
      }

      map<int, list<int>> adj = addEdge(vertex, edges);
      cout << endl << "Adjacency List is:" << endl;
      for(auto i : adj) {
          cout << i.first << "->";
          for(auto j : i.second) {
              cout << j << " ";
          }
          cout << endl;
      }
  }
  ```

## Notes

- This implementation assumes an undirected graph. If you want a directed graph, remove the line that adds `u` to `v` in the adjacency list.
- Ensure that the vertices are numbered consecutively from `0` to `vertex - 1`.
  
