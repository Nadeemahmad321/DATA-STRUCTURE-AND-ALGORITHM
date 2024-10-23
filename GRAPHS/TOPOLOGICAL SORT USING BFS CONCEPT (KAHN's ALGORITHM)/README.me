# Topological Sort Using Kahn's Algorithm

This program implements a topological sort algorithm using Kahn's Algorithm, which is based on the BFS (Breadth-First Search) concept. It is designed to work with directed acyclic graphs (DAGs).

## Description

Topological sorting is a linear ordering of vertices such that for every directed edge \( (u, v) \), vertex \( u \) comes before vertex \( v \) in the ordering. Kahn's Algorithm is an efficient method to achieve this.

## Key Concepts

- **Directed Acyclic Graph (DAG)**: A graph that is directed and contains no cycles. This property is crucial for topological sorting.
- **Indegree**: The number of edges directed into a vertex. In topological sorting, vertices with an indegree of 0 are processed first.

## Code Explanation

### Key Functions

1. **`topoLogicalSort(int vertex, vector<vector<int>>& edges)`**:
   - **Input**:
     - `vertex`: Number of vertices in the graph.
     - `edges`: A vector of pairs representing directed edges.
   - **Output**:
     - A vector containing the topologically sorted order of vertices.

2. **Main Function**:
   - Takes user input for the number of vertices and edges.
   - Constructs the edges and calls the `topoLogicalSort` function.
   - Outputs the topologically sorted order.

### Algorithm Steps

1. **Adjacency List Creation**:
   - Construct an adjacency list from the given edges.

2. **Indegree Calculation**:
   - Compute the indegree (number of incoming edges) for each vertex.

3. **Queue Initialization**:
   - Initialize a queue and enqueue all vertices with an indegree of 0.

4. **BFS Traversal**:
   - While the queue is not empty:
     - Dequeue a vertex and add it to the result list.
     - Decrease the indegree of its neighbors and enqueue any that reach an indegree of 0.

## Example

### Input Graph

Consider the following directed graph represented by the edges:

```
5 → 2
5 → 0
4 → 0
4 → 1
2 → 3
3 → 1
```

This can be visualized as:

```
     5
    / \
   v   v
   2   0
   |
   v
   3 → 1
   |
   v
   4
```

### Example Input

```
Enter the number of vertex: 6
Enter the number of edgeCount: 6
Enter edge (u v):
5 2
5 0
4 0
4 1
2 3
3 1
```

### Explanation of Execution

1. **Adjacency List Creation**:
   ```
   {
       5: [2, 0],
       4: [0, 1],
       2: [3],
       3: [1]
   }
   ```

2. **Indegree Calculation**:
   - Vertex 0: indegree = 2 (from 5 and 4)
   - Vertex 1: indegree = 2 (from 4 and 3)
   - Vertex 2: indegree = 1 (from 5)
   - Vertex 3: indegree = 1 (from 2)
   - Vertex 4: indegree = 0
   - Vertex 5: indegree = 0

   Resulting indegree array: `[2, 2, 1, 1, 0, 0]`

3. **Queue Initialization**:
   - Enqueue vertices with indegree 0: `{4, 5}`

4. **BFS Traversal**:
   - Dequeue 4: `ans = [4]`, decrease indegrees of 0 and 1.
   - New indegrees: `[1, 1, 1, 1, 0, 0]`, enqueue 5: `{5}`
   - Dequeue 5: `ans = [4, 5]`, decrease indegrees of 2 and 0.
   - New indegrees: `[0, 1, 0, 1, 0, 0]`, enqueue 0, 2: `{0, 2}`
   - Dequeue 0: `ans = [4, 5, 0]`
   - Dequeue 2: `ans = [4, 5, 0, 2]`, decrease indegree of 3.
   - New indegree for 3: 0, enqueue 3: `{3}`
   - Dequeue 3: `ans = [4, 5, 0, 2, 3]`, decrease indegree of 1.
   - New indegree for 1: 1.
   - Dequeue remaining nodes until the queue is empty.

Final sorted order: `4, 5, 0, 2, 3, 1`.

### Example Output

```
Topological sort is: 4 5 0 2 3 1
```

## Important Information

- Ensure that the input graph is a directed acyclic graph (DAG); otherwise, the topological sort is not defined.
- The program assumes vertices are labeled from `0` to `vertex-1`.

## Usage

1. Compile the code using a C++ compiler:
   ```bash
   g++ topological_sort.cpp -o topological_sort
   ```

2. Run the compiled program:
   ```bash
   ./topological_sort
   ```

3. Input the number of vertices and edges followed by the edges themselves in the format `u v`.
