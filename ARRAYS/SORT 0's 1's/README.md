# Sorting Array of 0s and 1s

## Overview
This program sorts an array consisting of only 0s and 1s using an efficient algorithm. It employs a two-pointer technique to achieve this in linear time complexity. This is a simple and effective solution for binary sorting.

## Features
- Efficiently sorts an array containing only 0s and 1s.
- Utilizes O(n) time complexity and O(1) space complexity.
- Provides clear input prompts and outputs the sorted array.

## How It Works
The program uses two pointers:
1. **Pointer `i`** starts from the beginning of the array and moves right until it finds a 1.
2. **Pointer `j`** starts from the end of the array and moves left until it finds a 0.

The algorithm continues to swap elements at these pointers until they meet. This way, all 0s will be moved to the front and all 1s to the back of the array.

## Code Explanation

### Functions
- **`void print(const vector<int>& arr)`**: Prints the elements of the array.
- **`void sorting(vector<int>& arr)`**: Sorts the array in place using the two-pointer technique.

### Main Function
The `main()` function handles user input and output:
1. Prompts the user for the size of the array.
2. Reads the elements (only 0s and 1s).
3. Calls the sorting function and prints the sorted result.

## Example

### Input
```
Enter the size of the vector: 10
Enter the elements of the array (0s and 1s only): 
1
0
1
0
0
1
1
0
0
1
```

### Step-by-Step Sorting Process
1. **Initial State**:
   - Array: `[1, 0, 1, 0, 0, 1, 1, 0, 0, 1]`
   - `i = 0`, `j = 9` (indices of the first and last elements)

2. **First Iteration**:
   - Increment `i` until it points to a 1: `i` moves to index 0 (1), index 1 (0) (stop here).
   - Decrement `j` until it points to a 0: `j` moves to index 9 (1), index 8 (0) (stop here).
   - Since `i < j`, swap `arr[i]` and `arr[j]`:
   - Array after swap: `[0, 0, 1, 0, 0, 1, 1, 0, 1, 1]`
   - Update `i` and `j`: `i = 1`, `j = 8`

3. **Second Iteration**:
   - Increment `i` until it points to a 1: `i` moves to index 1 (0), index 2 (1) (stop here).
   - Decrement `j` until it points to a 0: `j` moves to index 8 (1), index 7 (0) (stop here).
   - Since `i < j`, swap `arr[i]` and `arr[j]`:
   - Array after swap: `[0, 0, 0, 1, 0, 1, 1, 1, 1, 1]`
   - Update `i` and `j`: `i = 3`, `j = 7`

4. **Third Iteration**:
   - Increment `i` until it points to a 1: `i` moves to index 3 (1) (stop here).
   - Decrement `j` until it points to a 0: `j` moves to index 7 (1), index 6 (1), index 5 (1), index 4 (0) (stop here).
   - Since `i < j`, swap `arr[i]` and `arr[j]`:
   - Array after swap: `[0, 0, 0, 0, 1, 1, 1, 1, 1, 1]`
   - Update `i` and `j`: `i = 4`, `j = 4`

5. **Termination**:
   - Now, `i` is no longer less than `j`, so the loop terminates.

### Final Output
```
After sorting: 
0 0 0 0 1 1 1 1 1 1 
```

### Explanation of Output
- The program sorts the input array such that all 0s are on the left and all 1s are on the right. The sorted output is displayed.

## Complexity
- **Time Complexity**: O(n)
  - The algorithm makes a single pass through the array, where `n` is the number of elements. Each element is processed at most once, resulting in linear time complexity.
  
- **Space Complexity**: O(1)
  - The sorting is performed in place, meaning no additional data structures proportional to the size of the input are used. Only a few variables are needed for indexing, which leads to constant space complexity.

## Compilation and Execution
To compile and run the program, use the following commands in your terminal:
```bash
g++ -o sort_binary sort_binary.cpp
./sort_binary
```
