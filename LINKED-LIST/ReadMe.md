```markdown
# Linked List Data Structure in C++

This repository contains a C++ implementation of various types of linked lists.
A linked list is a fundamental data structure that consists of a sequence of elements where each element points to the next one.
 This allows for efficient insertions and deletions.

## Types of Linked Lists

### 1. Singly Linked List

A singly linked list is a type of linked list where each node points to the next node in the sequence.
 It has a head pointer that points to the first node and each node contains a data value and a pointer to the next node.

### 2. Doubly Linked List

A doubly linked list is a type of linked list where each node points to both the next and the previous node.
This allows for traversal in both directions (forward and backward). Each node has three parts: a data value, a pointer to the next node, and a pointer to the previous node.

### 3. Circular Linked List

A circular linked list is a variation where the last node points back to the first node, forming a circle.
 It can be either singly or doubly circular. This type of list is useful for applications that require a circular iteration through the list.

### 4. Doubly Circular Linked List

A doubly circular linked list is a type of circular linked list where each node points to both the next and the previous node,
 and the last node points back to the first node, while the first node points back to the last node.

## Features

- **Insertion**: Efficient insertion of elements at the beginning, end, or at a specific position.
- **Deletion**: Efficient deletion of elements from the beginning, end, or a specific position.
- **Traversal**: Methods to traverse the list and access elements.
- **Search**: Methods to search for elements in the list.



## Usage

1. **Create an instance of the desired linked list class.**
2. **Use `insert` methods to add elements.**
3. **Use `deleteNode` methods to remove elements.**
4. **Use `display` methods to print the list.**
