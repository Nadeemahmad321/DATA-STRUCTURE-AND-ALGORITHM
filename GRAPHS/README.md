# Graph Data Structure

## Overview

A graph is a collection of nodes (or vertices) and edges that connect pairs of nodes. 
Graphs are widely used in computer science to model relationships between entities, such as social networks, transportation systems, and more.

## Table of Contents

- [Types of Graphs](#types-of-graphs)
- [Graph Representation](#graph-representation)
- [Common Operations](#common-operations)
- [Algorithms](#algorithms)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Types of Graphs

1. **Directed Graph**: A graph where edges have a direction, indicating the relationship flows from one vertex to another.
2. **Undirected Graph**: A graph where edges do not have a direction; the relationship is bidirectional.
3. **Weighted Graph**: A graph where edges have weights (or costs) associated with them.
4. **Unweighted Graph**: A graph where all edges are considered equal.
5. **Cyclic Graph**: A graph that contains at least one cycle (a path that starts and ends at the same vertex).
6. **Acyclic Graph**: A graph that does not contain any cycles.

## Graph Representation

Graphs can be represented in various ways, including:

1. **Adjacency Matrix**: A 2D array where the cell at row `i` and column `j` indicates the presence (and weight) of an edge between vertex `i` and vertex `j`.
2. **Adjacency List**: An array (or list) of lists where each list at index `i` contains the neighbors of vertex `i`.

### Example

```plaintext
Adjacency Matrix:
    A  B  C
A [ 0, 1, 0 ]
B [ 1, 0, 1 ]
C [ 0, 1, 0 ]

Adjacency List:
A -> B
B -> A -> C
C -> B
```

## Common Operations

- **Add Vertex**: Add a new vertex to the graph.
- **Add Edge**: Connect two vertices with an edge.
- **Remove Vertex**: Remove a vertex and its associated edges.
- **Remove Edge**: Disconnect two vertices.

## Algorithms

Here are some common algorithms that can be applied to graphs:

1. **Depth-First Search (DFS)**: A traversal algorithm that explores as far down a branch as possible before backtracking.
2. **Breadth-First Search (BFS)**: A traversal algorithm that explores all neighbors at the present depth before moving on to nodes at the next depth level.
3. **Dijkstra's Algorithm**: An algorithm for finding the shortest paths between nodes in a weighted graph.
4. **Kruskal's Algorithm**: An algorithm for finding the minimum spanning tree of a graph.

