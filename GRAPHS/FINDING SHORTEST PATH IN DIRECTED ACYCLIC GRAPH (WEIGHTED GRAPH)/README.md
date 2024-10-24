# Shortest Path in Directed Acyclic Graph (Weighted Graph)

This program implements an algorithm to find the shortest path in a directed acyclic graph (DAG) using topological sorting and dynamic programming. The algorithm efficiently calculates the shortest distance from a specified source node to all other nodes in the graph.

## Table of Contents

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Usage](#usage)
- [Code Explanation](#code-explanation)
- [Example](#example)
- [Graph Illustration](#graph-illustration)
- [Important Information](#important-information)

## Features

- Handles directed acyclic graphs (DAGs) with weighted edges.
- Uses Depth First Search (DFS) for topological sorting.
- Computes the shortest path from a specified source node.
- Displays the shortest distances to all nodes from the source.

## Prerequisites

Make sure you have the following installed:
- A C++ compiler (e.g., g++, clang++)
- Basic understanding of graphs, especially directed graphs.

## Usage

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. Compile the program:
   ```bash
   g++ -o shortest_path shortest_path.cpp
   ```

3. Run the program:
   ```bash
   ./shortest_path
   ```

4. Follow the prompts to input the number of vertices, edges, and their respective weights.

## Code Explanation

The program consists of several key functions and procedures. Here’s a breakdown of the main components:

### 1. Depth First Search for Topological Sorting

```cpp
void dfs(unordered_map<int,list<pair<int,int>>>& adjList, unordered_map<int,bool>& visited, stack<int>& s, int node) {
    visited[node] = true;  // Mark the node as visited
    for (auto neighbour : adjList[node]) {
        if (!visited[neighbour.first]) {  // If the neighbour has not been visited
            dfs(adjList, visited, s, neighbour.first);  // Recur for the neighbour
        }
    }
    s.push(node);  // Push the current node to the stack after visiting all neighbours
}
```

### 2. Get Shortest Path

```cpp
void getShortestPath(int src, vector<int>& dist, stack<int>& s, unordered_map<int, list<pair<int, int>>>& adjList) {
    dist[src] = 0;  // Initialize the source node distance to 0
    while (!s.empty()) {
        int top = s.top();  // Get the top node from the stack
        s.pop();
        if (dist[top] != INT_MAX) {  // If the node has a valid distance
            for (auto i : adjList[top]) {  // Traverse its neighbours
                if (dist[top] + i.second < dist[i.first]) {  // Relaxation step
                    dist[i.first] = dist[top] + i.second;  // Update distance
                }
            }
        }
    }
}
```

### 3. Finding Shortest Path

```cpp
vector<int> findingShortestPath(int vertex, vector<vector<int>>& edges) {
    unordered_map<int, list<pair<int, int>>> adjList;  // Adjacency list
    for (int i = 0; i < edges.size(); i++) {
        int u = edges[i][0], v = edges[i][1], wt = edges[i][2];  // Extract edge information
        adjList[u].push_back({v, wt});  // Add edge to the adjacency list
    }

    stack<int> s;  // Stack to hold the topological sort
    unordered_map<int, bool> visited;  // To track visited nodes
    for (int i = 0; i < vertex; i++) {
        if (!visited[i]) {
            dfs(adjList, visited, s, i);  // Perform DFS for topological sort
        }
    }

    int sourceNode;
    cout << "Enter the source node: ";
    cin >> sourceNode;

    vector<int> distance(vertex, INT_MAX);  // Initialize distances
    getShortestPath(sourceNode, distance, s, adjList);  // Get shortest paths
    return distance;  // Return the distances
}
```

### 4. Main Function

```cpp
int main() {
    int vertex, edgeCount;
    cout << "Enter the number of vertices: ";
    cin >> vertex;
    cout << "Enter the number of edges: ";
    cin >> edgeCount;

    vector<vector<int>> edges(edgeCount, vector<int>(3));  // Edge list
    cout << "Enter the edges (u v w):" << endl;
    for (int i = 0; i < edgeCount; i++) {
        cin >> edges[i][0] >> edges[i][1] >> edges[i][2];  // Read edges
    }

    vector<int> shortPath = findingShortestPath(vertex, edges);  // Calculate shortest paths

    cout << "Shortest distances: ";
    for (auto i : shortPath) {
        cout << i << " ";  // Output shortest distances
    }
    return 0;
}
```

## Example

### Input:
```
Enter the number of vertices: 5
Enter the number of edges: 6
Enter the edges (u v w):
0 1 2
0 2 3
1 3 1
2 3 2
1 4 3
3 4 1
Enter the source node: 0
```

### Explanation:
- The graph has 5 vertices and 6 directed edges with weights.
- The edges are as follows:
  - 0 → 1 with weight 2
  - 0 → 2 with weight 3
  - 1 → 3 with weight 1
  - 2 → 3 with weight 2
  - 1 → 4 with weight 3
  - 3 → 4 with weight 1

### Output:
```
Shortest distances: 0 2 3 3 6 
```

### Explanation of Output:
- The shortest distance from the source node (0) to:
  - Node 0: 0 (itself)
  - Node 1: 2 (via edge 0 → 1)
  - Node 2: 3 (via edge 0 → 2)
  - Node 3: 3 (via path 0 → 1 → 3 or 0 → 2 → 3)
  - Node 4: 6 (via path 0 → 1 → 4)

## Graph Illustration

Here's a visual representation of the directed acyclic graph based on the input:

```
   (0)
   / \
 2/   \3
 /     \
(1)     (2)
 | \    /
1 |  \ 2
 |   \ /
(3)---(4)
  \1
```

## Important Information

- **Directed Acyclic Graph (DAG)**: A graph that is directed and contains no cycles. This property ensures that topological sorting is possible.
- **Topological Sorting**: A linear ordering of vertices such that for every directed edge \( u \to v \), vertex \( u \) comes before \( v \).
- **Relaxation**: The process of updating the shortest path estimate. If a shorter path to a vertex is found, its distance is updated.
