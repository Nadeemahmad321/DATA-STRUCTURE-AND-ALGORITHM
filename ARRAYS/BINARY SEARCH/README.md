# Binary Search Implementation in C++

This repository contains a simple implementation of the Binary Search algorithm in C++. The program takes a sorted array and searches for a specified element using binary search.

## Table of Contents

- [Introduction](#introduction)
- [How Binary Search Works](#how-binary-search-works)
- [Complexity Analysis](#complexity-analysis)
- [Usage](#usage)
- [Code Explanation](#code-explanation)
- [Example](#example)
- [Requirements](#requirements)

## Introduction

Binary search is an efficient algorithm for finding an item from a sorted list of items. Unlike linear search, which checks each element sequentially, binary search works by dividing the search interval in half repeatedly, which drastically reduces the number of comparisons needed.

## How Binary Search Works

1. **Initial Setup**: Define the start and end indices of the search range. Calculate the middle index.
2. **Comparison**:
   - If the middle element is equal to the key, return the index (or true).
   - If the key is less than the middle element, narrow the search to the left half of the array.
   - If the key is greater than the middle element, narrow the search to the right half.
3. **Repeat**: Continue this process until the key is found or the search range is invalid (i.e., the start index exceeds the end index).

## Complexity Analysis

- **Time Complexity**: \(O(\log n)\)
  - Each comparison cuts the search space in half, leading to logarithmic growth with respect to the number of elements.
  
- **Space Complexity**: \(O(1)\)
  - The algorithm uses a constant amount of space, as it only requires a few variables for tracking indices.

## Usage

1. Clone this repository or download the source code.
2. Compile the program using a C++ compiler. For example:
   ```bash
   g++ binary_search.cpp -o binary_search
   ```
3. Run the executable:
   ```bash
   ./binary_search
   ```
4. Enter the size of the array.
5. Input the elements of the array (must be sorted).
6. Enter the element you want to search for.

## Code Explanation

The program consists of the following main components:

- **binarySearch Function**: This function takes an array, its size, and the key to be searched. It performs the binary search algorithm and returns `true` if the key is found and `false` otherwise.

- **Main Function**: 
  - Prompts the user to input the size and elements of the array.
  - Calls the `binarySearch` function with the user-defined key.
  - Outputs whether the key was found or not.

### Code Snippet
```cpp
bool binarySearch(int arr[], int size, int key) {
    // Implementation of binary search...
}
```

## Example

Let's consider a practical example to illustrate how binary search works.

### Example Scenario

Suppose we have the following sorted array:

```
Array: [2, 5, 8, 12, 16, 23, 38, 45, 56, 72]
```

And we want to search for the element `23`.

### Step-by-Step Explanation

1. **Initial Indices**:
   - Start = 0
   - End = 9 (length of array - 1)
   - Mid = (0 + 9) / 2 = 4 (value = 16)

2. **First Comparison**:
   - `23 > 16`: Move to the right half.
   - Update Start = 5

3. **Recalculate Mid**:
   - Mid = (5 + 9) / 2 = 7 (value = 45)

4. **Second Comparison**:
   - `23 < 45`: Move to the left half.
   - Update End = 6

5. **Recalculate Mid**:
   - Mid = (5 + 6) / 2 = 5 (value = 23)

6. **Third Comparison**:
   - `23 == 23`: Element found.

The function returns `true`, indicating that the element `23` is present in the array.

## Requirements

- A C++ compiler (e.g., g++, clang++)
- Basic knowledge of C++ programming
