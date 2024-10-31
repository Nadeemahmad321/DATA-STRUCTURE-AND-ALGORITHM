# First and Last Occurrence of Element in a Sorted Array

This program finds the first and last occurrences of a given element (key) in a sorted array using binary search. The time complexity of the algorithm is O(log n), making it efficient for large datasets.

## Features

- Efficiently finds the first occurrence of an element in a sorted array.
- Efficiently finds the last occurrence of an element in a sorted array.
- Handles input validation for the size of the array.

## Usage

### Prerequisites

Make sure you have a C++ compiler installed. You can use any IDE or compiler like g++, Code::Blocks, or Visual Studio.

### Compilation

To compile the program, use the following command:

```bash
g++ -o find_occurrences find_occurrences.cpp
```

### Running the Program

Run the compiled program using the command:

```bash
./find_occurrences
```

### Input

1. Enter the size of the vector (must be a positive integer).
2. Enter the elements of the vector (the elements must be sorted).
3. Enter the key (the element to search for).

### Output

The program will output the indices of the first and last occurrences of the specified key. If the key is not found, it will return `-1`.

## Complexity

- **Time Complexity**: O(log n) for both `firstOccurrence` and `lastOccurrence` functions due to the binary search approach.
- **Space Complexity**: O(1) as no additional space is used apart from variables.

## Step-by-Step Example

### Example Input

Let's consider the following input:

```
Size of vector: 7
Elements of vector: 1 2 2 2 3 4 5
Key to search: 2
```

### Step-by-Step Execution

1. **Initialization**:
   - The program initializes the `start` to 0 and `end` to 6 (the last index of the array).
   - The variable `ans` is initialized to -1.

2. **Finding the First Occurrence**:
   - **First Iteration**:
     - Calculate `mid = (0 + 6) / 2 = 3`. The middle element is `arr[3] = 2`.
     - Since `arr[3]` equals the key (2), update `ans` to 3, and set `end` to `mid - 1 = 2` to search the left side for earlier occurrences.

   - **Second Iteration**:
     - Calculate `mid = (0 + 2) / 2 = 1`. The middle element is `arr[1] = 2`.
     - Again, `arr[1]` equals the key, so update `ans` to 1 and set `end` to `mid - 1 = 0`.

   - **Third Iteration**:
     - Calculate `mid = (0 + 0) / 2 = 0`. The middle element is `arr[0] = 1`.
     - Since `arr[0]` is less than the key, set `start` to `mid + 1 = 1`.
   
   - The loop terminates when `start` exceeds `end`. The first occurrence is at index 1.

3. **Finding the Last Occurrence**:
   - Reset `start` to 0 and `end` to 6. Initialize `ans` to -1.

   - **First Iteration**:
     - Calculate `mid = (0 + 6) / 2 = 3`. The middle element is `arr[3] = 2`.
     - Since `arr[3]` equals the key, update `ans` to 3, and set `start` to `mid + 1 = 4` to search the right side for later occurrences.

   - **Second Iteration**:
     - Calculate `mid = (4 + 6) / 2 = 5`. The middle element is `arr[5] = 4`.
     - Since `arr[5]` is greater than the key, set `end` to `mid - 1 = 4`.

   - **Third Iteration**:
     - Calculate `mid = (4 + 4) / 2 = 4`. The middle element is `arr[4] = 3`.
     - Since `arr[4]` is greater than the key, set `end` to `mid - 1 = 3`.

   - The loop terminates when `start` exceeds `end`. The last occurrence is at index 3.

### Final Output

The output will be:

```
First occurrence is at index: 1
Last occurrence is at index: 3
```

## Important Information

- The input array must be sorted for the binary search algorithm to work correctly.
- The program validates the array size to prevent errors.
- If the key is not found, both first and last occurrences will return `-1`.
