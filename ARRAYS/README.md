# Arrays

## Overview

An array is a collection of variables of the same type that are accessed using a common name. In C++, arrays are essential for managing collections of data efficiently and allow for quick access to elements through indexing.

## Table of Contents

- [1. Definition](#1-definition)
- [2. Characteristics](#2-characteristics)
- [3. Types of Arrays](#3-types-of-arrays)
  - [3.1. One-Dimensional Arrays](#31-one-dimensional-arrays)
  - [3.2. Multi-Dimensional Arrays](#32-multi-dimensional-arrays)
- [4. Array Initialization](#4-array-initialization)
- [5. Array Operations](#5-array-operations)
  - [5.1. Accessing Elements](#51-accessing-elements)
  - [5.2. Inserting Elements](#52-inserting-elements)
  - [5.3. Deleting Elements](#53-deleting-elements)
  - [5.4. Traversing Arrays](#54-traversing-arrays)
- [6. Common Array Algorithms](#6-common-array-algorithms)
  - [6.1. Searching Algorithms](#61-searching-algorithms)
  - [6.2. Sorting Algorithms](#62-sorting-algorithms)
- [7. Advantages of Arrays](#7-advantages-of-arrays)
- [8. Disadvantages of Arrays](#8-disadvantages-of-arrays)
- [9. Conclusion](#9-conclusion)
- [10. References](#10-references)

## 1. Definition

An **array** in C++ is a collection of elements of the same data type stored in contiguous memory locations. The elements can be accessed using their index, which starts from 0.

## 2. Characteristics

- **Fixed Size**: The size of the array is determined at compile time and cannot be changed at runtime.
- **Homogeneous Elements**: All elements in an array must be of the same data type.
- **Index-Based Access**: Elements are accessed using an index, starting from 0.
- **Contiguous Memory Allocation**: Arrays are stored in contiguous memory locations, which allows for efficient access.

## 3. Types of Arrays

### 3.1. One-Dimensional Arrays

A one-dimensional array is a linear structure that holds a sequence of elements.

**Example:**

```cpp
int arr[5] = {1, 2, 3, 4, 5};
```

### 3.2. Multi-Dimensional Arrays

Multi-dimensional arrays can hold data in more than one dimension (e.g., 2D arrays).

**Example of a 2D Array:**

```cpp
int matrix[3][3] = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};
```

## 4. Array Initialization

Arrays can be initialized at the time of declaration, and there are different methods to do so:

- **Static Initialization**:

```cpp
int arr[5] = {1, 2, 3, 4, 5}; // Initializes all elements
```

- **Partial Initialization**:

```cpp
int arr[5] = {1, 2}; // Initializes first two elements, others are set to 0
```

- **Dynamic Initialization** (using `new`):

```cpp
int* dynamicArr = new int[5]; // Dynamically allocated array of size 5
```

## 5. Array Operations

### 5.1. Accessing Elements

You can access elements in an array using their index.

**Example:**

```cpp
int x = arr[2];  // Accesses the third element (value 3)
```

### 5.2. Inserting Elements

To insert an element, you assign a value to a specific index.

**Example:**

```cpp
arr[0] = 10;  // Changes the first element to 10
```

### 5.3. Deleting Elements

To "delete" an element, set it to a default value, as C++ does not support dynamic resizing of arrays.

**Example:**

```cpp
arr[2] = 0;  // Sets the third element to 0
```

### 5.4. Traversing Arrays

You can traverse an array using a loop.

**Example:**

```cpp
for (int i = 0; i < 5; i++) {
    std::cout << arr[i] << " ";
}
```

## 6. Common Array Algorithms

### 6.1. Searching Algorithms

- **Linear Search**: Simple search method that checks each element.

```cpp
int linearSearch(int arr[], int size, int target) {
    for (int i = 0; i < size; i++) {
        if (arr[i] == target) {
            return i; // Returns index if found
        }
    }
    return -1; // Not found
}
```

- **Binary Search**: Efficient search method for sorted arrays.

```cpp
int binarySearch(int arr[], int size, int target) {
    int left = 0, right = size - 1;
    while (left <= right) {
        int mid = left + (right - left) / 2;
        if (arr[mid] == target) return mid;
        if (arr[mid] < target) left = mid + 1;
        else right = mid - 1;
    }
    return -1; // Not found
}
```

### 6.2. Sorting Algorithms

- **Bubble Sort**: Simple sorting algorithm.

```cpp
void bubbleSort(int arr[], int size) {
    for (int i = 0; i < size - 1; i++) {
        for (int j = 0; j < size - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                std::swap(arr[j], arr[j + 1]);
            }
        }
    }
}
```

- **Selection Sort**: Another basic sorting algorithm.

```cpp
void selectionSort(int arr[], int size) {
    for (int i = 0; i < size - 1; i++) {
        int minIndex = i;
        for (int j = i + 1; j < size; j++) {
            if (arr[j] < arr[minIndex]) {
                minIndex = j;
            }
        }
        std::swap(arr[i], arr[minIndex]);
    }
}
```

## 7. Advantages of Arrays

- **Efficient Access**: Accessing elements by index is done in constant time, O(1).
- **Memory Efficiency**: Arrays have less overhead compared to dynamic structures like linked lists.
- **Easy to Traverse**: Looping through arrays is straightforward.
- **Cache Friendly**: Contiguous memory allocation can enhance cache performance.

## 8. Disadvantages of Arrays

- **Fixed Size**: The size is static; you cannot dynamically add or remove elements.
- **Costly Insertion/Deletion**: Operations that require shifting elements can be inefficient (O(n)).
- **Homogeneous**: All elements must be of the same data type.
- **Memory Waste**: If the allocated size is larger than needed, it can lead to memory wastage.

## 9. Conclusion

Arrays are a fundamental data structure in C++ that provide a way to store and manage collections of data efficiently. While they have limitations, understanding arrays is crucial for effective programming and algorithm development in C++. They form the basis for more complex data structures and algorithms.

## 10. References

- [C++ Documentation - Arrays](https://en.cppreference.com/w/cpp/language/array)
- [GeeksforGeeks - C++ Arrays](https://www.geeksforgeeks.org/arrays-in-c-cpp/)
- [TutorialsPoint - C++ Arrays](https://www.tutorialspoint.com/cplusplus/cpp_arrays.htm)
```
