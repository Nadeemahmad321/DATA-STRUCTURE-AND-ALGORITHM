# Kruskal's Algorithm

This program implements Kruskal's algorithm to find the minimum spanning tree (MST) of a graph. The algorithm efficiently selects edges to minimize the total weight while avoiding cycles.

## Overview

Kruskal's algorithm works by sorting all edges of the graph by their weights and adding them to the MST one by one, ensuring that no cycles are formed until the MST has `V-1` edges, where `V` is the number of vertices.

## Example Graph

### Graph Representation

Consider the following graph:

```
    (0)
   / | \
10/  | \6
 /   |  \
(1)--(2)--(3)
 |    |   |
15    |   |4
 |    |   |
(3)---(2)---(1)
```

### Edges and Weights

The edges of the graph are represented as follows:

- (0, 1, 10)
- (0, 2, 6)
- (0, 3, 5)
- (1, 3, 15)
- (2, 3, 4)

### Input Format

1. Number of vertices: 4
2. Number of edges: 5
3. Each edge: 
   - `0 1 10`
   - `0 2 6`
   - `0 3 5`
   - `1 3 15`
   - `2 3 4`

## Steps in Kruskal's Algorithm

### Step 1: Initialization

1. **Create a Set for Each Vertex**:
   - Each vertex is initially its own parent, and the rank is set to 0.

   ```cpp
   makeSet(parent, rank, vertex);
   ```

### Step 2: Sort Edges

2. **Sort the Edges**:
   - Sort all edges based on their weights.

   ```cpp
   sort(edges.begin(), edges.end(), cmp);
   ```

   After sorting, the edges will be in this order:
   - (2, 3, 4)
   - (0, 3, 5)
   - (0, 2, 6)
   - (0, 1, 10)
   - (1, 3, 15)

### Step 3: Process Each Edge

3. **Iterate Over Sorted Edges**:
   - For each edge, check if the vertices are in the same component using `findParent`.
   - If they are in different components, add the edge to the MST and unite the components using `unionSet`.

   ```cpp
   for(int i = 0; i < edges.size(); i++) {
       int u = findParent(parent, edges[i][0]);
       int v = findParent(parent, edges[i][1]);
       if (u != v) {
           minWeight += edges[i][2];
           unionSet(u, v, parent, rank);
       }
   }
   ```

### Step 4: Calculate Minimum Cost

4. **Calculate Total Weight**:
   - The total weight of the edges included in the MST is accumulated.

## Final Output

After processing all edges, the program will output the minimum spanning cost:

```
Minimum spanning cost is: 19
```

### Important Information

- **Time Complexity**: O(E log E) due to sorting the edges, where E is the number of edges. The union-find operations run in nearly constant time, O(α(V)).
- **Space Complexity**: O(V) for storing the parent and rank arrays.
- **Cycle Detection**: The algorithm inherently prevents cycles by checking if two vertices belong to different components before adding an edge.

## Code Explanation

```cpp
#include<bits/stdc++.h>
using namespace std;

bool cmp(vector<int>&a, vector<int>&b) {
    return a[2] < b[2];
}

// Initialization
void makeSet(vector<int>& parent, vector<int>& rank, int vertex) {
    for (int i = 0; i < vertex; i++) {
        parent[i] = i; // Each vertex is its own parent
        rank[i] = 0;   // Initial rank is 0
    }
}

// Finding parent with path compression
int findParent(vector<int>& parent, int node) {
    if (parent[node] == node) {
        return node;        
    }
    return parent[node] = findParent(parent, parent[node]);
}

// Union operation
void unionSet(int u, int v, vector<int>& parent, vector<int>& rank) {
    u = findParent(parent, u);
    v = findParent(parent, v);
    
    if (rank[u] < rank[v]) {
        parent[u] = v;
    } else if (rank[v] < rank[u]) {
        parent[v] = u;
    } else {
        parent[v] = u; // Arbitrarily choose u as the root
        rank[u]++;     // Increase rank if they were equal
    }
}

// Minimum spanning tree
int minimumSpanningTree(int vertex, vector<vector<int>>& edges) {
    sort(edges.begin(), edges.end(), cmp);
    vector<int> parent(vertex);
    vector<int> rank(vertex);
    makeSet(parent, rank, vertex);
    
    int minWeight = 0;
    for (int i = 0; i < edges.size(); i++) {
        int u = findParent(parent, edges[i][0]);
        int v = findParent(parent, edges[i][1]);
        int weight = edges[i][2];
        
        if (u != v) {
            minWeight += weight; // Add weight to MST
            unionSet(u, v, parent, rank);
        }
    }
    return minWeight;
}

int main() {
    int vertex, edgeCount;
    cout << "Enter the number of vertex: ";
    cin >> vertex;
    cout << "Enter the number of edgeCount: ";
    cin >> edgeCount;
    vector<vector<int>> edges(edgeCount, vector<int>(3));
    
    for (int i = 0; i < edgeCount; i++) {
        cin >> edges[i][0] >> edges[i][1] >> edges[i][2];
    }
    
    int ans = minimumSpanningTree(vertex, edges);
    cout << "Minimum spanning cost is: " << ans << endl;
}
```
