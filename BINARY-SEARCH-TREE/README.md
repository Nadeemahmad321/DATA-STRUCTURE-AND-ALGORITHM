# Binary Search Tree (BST)

## Overview

A Binary Search Tree (BST) is a hierarchical data structure that allows for efficient insertion, deletion, and lookup of values. Each node has up to two children: 
the left child contains values less than the parent node, while the right child contains values greater than the parent node. This property enables fast searching and maintaining sorted order.

### Key Properties

- **Node Structure**: Each node contains a value, a reference to the left child, and a reference to the right child.
- **Sorted Order**: In-order traversal of a BST yields values in ascending order.
- **Height-Balanced**: Ideally, a BST should be balanced to maintain O(log n) time complexity for operations.

## Common Operations

- **Insertion**: Adding a new value while maintaining the BST properties.
- **Deletion**: Removing a value while ensuring the BST structure remains valid.
- **Searching**: Finding a value by traversing the tree based on comparisons.

## Common Questions

1. **What is the time complexity of common operations in a BST?**
   - **Search**: O(h), where h is the height of the tree (O(log n) for balanced trees, O(n) for unbalanced).
   - **Insertion**: O(h).
   - **Deletion**: O(h).

2. **What happens when a BST becomes unbalanced?**
   - Performance degrades to O(n) for operations. To maintain balance, self-balancing trees like AVL trees or Red-Black trees can be used.

3. **How can you determine if a tree is a BST?**
   - Perform an in-order traversal and check if the values are sorted in ascending order.

4. **What is the difference between a BST and a regular binary tree?**
   - A BST has specific properties that maintain order, while a binary tree does not enforce any order on its nodes.

5. **How do you find the minimum and maximum values in a BST?**
   - **Minimum**: Traverse to the leftmost node.
   - **Maximum**: Traverse to the rightmost node.

6. **Can a BST contain duplicate values?**
   - Typically, BSTs do not allow duplicates. However, variations exist that can handle duplicates in specific ways.

7. **What are the traversal methods for a BST?**
   - **In-order**: Left, Root, Right (produces sorted output).
   - **Pre-order**: Root, Left, Right (used for creating a copy).
   - **Post-order**: Left, Right, Root (used for deleting the tree).

8. **How do you delete a node from a BST?**
   - There are three cases:
     - **Leaf Node**: Simply remove it.
     - **One Child**: Replace the node with its child.
     - **Two Children**: Replace the node with its in-order predecessor or successor, then delete that node.
