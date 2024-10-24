# Bellman-Ford Algorithm

The Bellman-Ford algorithm is a powerful method for finding the shortest paths from a single source vertex to all other vertices in a weighted graph, especially when the graph may contain negative weight edges. This algorithm is also capable of detecting negative weight cycles, which can affect the shortest path calculations.

## Overview

### Key Features

- Handles graphs with negative weights.
- Detects negative weight cycles.
- Calculates the shortest path from a source vertex to a specific destination vertex or all vertices.

### Complexity

- Time Complexity: \(O(V \times E)\), where \(V\) is the number of vertices and \(E\) is the number of edges.
- Space Complexity: \(O(V)\) for storing distances.

## Example Graph

Consider the following directed graph:

```
    (1)
   /   \
  4     2
 /       \
(0) --- (-3) --> (2)
 \         /
  5       1
   \     /
    (3) 
```

### Graph Representation

- **Vertices**: 0, 1, 2, 3
- **Edges**:
  - (0, 1, 4)
  - (0, 3, 5)
  - (1, 2, 2)
  - (3, 2, 1)
  - (1, 3, -3) (This edge creates a negative cycle)

### Input for the Algorithm

1. **Number of Vertices**: 4
2. **Number of Edges**: 5
3. **Edges**: 
   - (0, 1, 4)
   - (0, 3, 5)
   - (1, 2, 2)
   - (3, 2, 1)
   - (1, 3, -3)
4. **Source Vertex**: 0
5. **Destination Vertex**: 2

## Step-by-Step Explanation

1. **Initialization**:
   - Set the distance from the source (0) to itself as 0: `distance[0] = 0`.
   - Set distances to all other vertices as infinity: `distance[1] = distance[2] = distance[3] = ∞`.

   Initial distance array:
   ```
   [0, ∞, ∞, ∞]
   ```

2. **Relaxation**:
   - For each vertex, iterate through all edges and relax them:
     - **First Pass**:
       - Edge (0, 1, 4): Update distance[1] = min(∞, 0 + 4) → distance[1] = 4.
       - Edge (0, 3, 5): Update distance[3] = min(∞, 0 + 5) → distance[3] = 5.
       - Edge (1, 2, 2): Update distance[2] = min(∞, 4 + 2) → distance[2] = 6.
       - Edge (3, 2, 1): Update distance[2] = min(6, 5 + 1) → distance[2] = 6 (no change).
       - Edge (1, 3, -3): Update distance[3] = min(5, 4 - 3) → distance[3] = 1.

     Distance array after first pass:
     ```
     [0, 4, 6, 1]
     ```

     - **Second Pass**:
       - No further updates occur in the second pass as all distances remain optimal.

     Final distance array after two passes:
     ```
     [0, 4, 6, 1]
     ```

3. **Negative Cycle Check**:
   - After the V-1 passes, perform one more iteration to check for negative weight cycles. If any distance can still be relaxed, a negative cycle exists.
   - During this pass, we detect the update in the edge (1, 3, -3), indicating a negative cycle.

### Output

- Since a negative cycle is detected, the output will indicate that no shortest path exists due to the cycle.

## Important Information

- **Negative Cycles**: A negative cycle can be detrimental as it allows for paths of indefinite negative length, which can affect the shortest path calculations.
- **Use Cases**: The Bellman-Ford algorithm is often used in scenarios such as:
  - Routing algorithms in networks where edge weights represent costs that can fluctuate.
  - Applications in financial networks where losses can create negative weights.
  
### Conclusion

The Bellman-Ford algorithm is a crucial tool in graph theory, enabling robust analysis of paths in complex networks. Its ability to handle negative weights makes it suitable for a variety of applications in computer science, economics, and network theory.
