# Heap Data Structure

## Table of Contents

- [Introduction](#introduction)
- [Types of Heaps](#types-of-heaps)
  - [Min Heap](#min-heap)
  - [Max Heap](#max-heap)
- [Heap Properties](#heap-properties)
- [Operations on Heaps](#operations-on-heaps)
  - [Insertion](#insertion)
  - [Deletion](#deletion)
  - [Heapify](#heapify)
- [Applications of Heaps](#applications-of-heaps)
- [Complexity Analysis](#complexity-analysis)
- [Conclusion](#conclusion)

## Introduction

A **heap** is a specialized tree-based data structure that satisfies the heap property. 
It is commonly used to implement priority queues and is critical in various algorithms, such as heapsort. Heaps can be visualized as complete binary trees and are typically represented using arrays.

## Types of Heaps

### Min Heap

In a Min Heap, the value of each node is less than or equal to the values of its children. This means that the smallest element is always at the root of the heap.

### Max Heap

In a Max Heap, the value of each node is greater than or equal to the values of its children. Here, the largest element is at the root.

## Heap Properties

1. **Complete Binary Tree**: A heap is a complete binary tree, meaning all levels are fully filled except possibly the last level, which is filled from left to right.
2. **Heap Property**: In a Min Heap, every parent node is less than or equal to its children; in a Max Heap, every parent node is greater than or equal to its children.

## Operations on Heaps

### Insertion

When inserting a new element, it is added at the end of the heap (the last position in the array). After insertion, the element is "bubbled up" to restore the heap property.

### Deletion

To delete the root element, it is removed, and the last element in the heap is placed at the root. The new root is then "bubbled down" to restore the heap property.

### Heapify

Heapify is the process of converting an arbitrary array into a heap. This can be achieved in a bottom-up manner to ensure that the heap property is maintained.

## Applications of Heaps

- **Priority Queues**: Heaps are often used to efficiently manage elements with priorities, allowing quick retrieval of the highest (or lowest) priority element.
- **Heapsort**: This is a comparison-based sorting algorithm that utilizes the heap data structure for sorting.
- **Graph Algorithms**: Heaps are employed in algorithms like Dijkstra’s and Prim’s for efficient minimum retrieval.

## Complexity Analysis

- **Insertion**: O(log n)
- **Deletion**: O(log n)
- **Heapify**: O(n)

## Conclusion

Heaps are powerful data structures that offer efficient ways to manage and retrieve elements based on priority. 
They are widely used in applications ranging from sorting algorithms to graph processing, making them a fundamental concept in computer science. 
