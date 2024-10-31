# Merge Two Sorted Arrays

This C++ program merges two sorted arrays into a single sorted array using a third array. It prompts the user to input the sizes and elements of the two arrays and then outputs the merged result.

## Features

- Merges two sorted integer arrays into one sorted array.
- Utilizes a two-pointer technique for efficient merging.
- Handles dynamic array sizes based on user input.

## Requirements

- A C++ compiler (e.g., g++, clang++)
- C++ Standard Library

## Usage

1. **Compile the Program:**

   Use the following command to compile the program:

   ```bash
   g++ -o merge_sorted_arrays merge_sorted_arrays.cpp
   ```

2. **Run the Program:**

   Execute the compiled program with the following command:

   ```bash
   ./merge_sorted_arrays
   ```

3. **Input:**

   - Enter the size of the first array (vector `a`).
   - Enter the sorted elements of the first array.
   - Enter the size of the second array (vector `b`).
   - Enter the sorted elements of the second array.

4. **Output:**

   The program will output the merged sorted array.

## Example

### Input

```plaintext
Enter the size of vector a: 3
Enter the elements of vector a (sorted): 1 3 5
Enter the size of vector b: 4
Enter the elements of vector b (sorted): 2 4 6 8
```

### Explanation of Input

- The first array (vector `a`) has 3 elements: `[1, 3, 5]`.
- The second array (vector `b`) has 4 elements: `[2, 4, 6, 8]`.

### Output

```plaintext
Merged vector: 1 2 3 4 5 6 8
```

### Explanation of Output

The merged sorted array combines the elements from both arrays in ascending order:
- Starting with the first element of each array:
  - Compare `1` (from `a`) and `2` (from `b`). `1` is smaller, so it goes first.
  - Next, compare `3` (from `a`) and `2` (from `b`). `2` is smaller, so it is added next.
  - Continue this process until all elements are merged, resulting in: `[1, 2, 3, 4, 5, 6, 8]`.

## Algorithm Complexity

- **Time Complexity**: O(n + m)
  - Where `n` is the size of the first array and `m` is the size of the second array. Each element is processed exactly once.

- **Space Complexity**: O(n + m)
  - The space required for the output array, which stores all elements from both input arrays.

## Important Information

- **Sorted Input Required**: The program assumes that both input arrays are sorted. If the arrays are not sorted, the output will not be correct.
- **Dynamic Array Sizes**: The program can handle arrays of varying sizes based on user input.

## Code Structure

- `mergeTwoSortedArray`: A function that takes two sorted vectors and merges them into one sorted vector.
- `main`: The function that handles user input and output, and calls the merging function.
