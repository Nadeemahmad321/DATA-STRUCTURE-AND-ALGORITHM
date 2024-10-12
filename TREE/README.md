# Tree Data Structure in C++

This repository contains a C++ implementation of various tree data structures, focusing on binary trees and binary search trees (BST). It also includes examples of binary tree traversal techniques.

## Table of Contents
- [Introduction](#introduction)
- [Binary Tree](#binary-tree)
- [Binary Tree Traversal](#binary-tree-traversal)
  - [In-Order Traversal](#in-order-traversal)
  - [Pre-Order Traversal](#pre-order-traversal)
  - [Post-Order Traversal](#post-order-traversal)
  - [Level-Order Traversal](#level-order-traversal)
- [Binary Search Tree](#binary-search-tree)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Introduction

A **tree** is a widely used data structure that simulates a hierarchical tree structure, with a root value and subtrees of children. Each tree consists of nodes connected by edges.
 Trees are used in various applications such as parsing expressions, searching data, and managing hierarchical information.

### Binary Tree

A **binary tree** is a type of tree in which each node has at most two children referred to as the left child and the right child.
Binary trees can be used to represent various data structures and algorithms.

### Binary Search Tree (BST)

A **binary search tree** is a binary tree with an additional constraint: for each node, the value of all the nodes in its left subtree must be less than its own value, and the value of all the nodes in its right subtree must be greater than its own value.
This property allows for efficient searching, insertion, and deletion operations.

## Binary Tree Traversal

Tree traversal is the process of visiting each node in the tree in a systematic way. There are several methods for traversing a binary tree:

### In-Order Traversal

In in-order traversal, the nodes are recursively visited in this order: left child, current node, right child.



### Pre-Order Traversal

In pre-order traversal, the nodes are recursively visited in this order: current node, left child, right child.



### Post-Order Traversal

In post-order traversal, the nodes are recursively visited in this order: left child, right child, current node.


### Level-Order Traversal

Level-order traversal visits each level of the tree from top to bottom and left to right. This is typically implemented using a queue.



## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue for any enhancements or bugs.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
