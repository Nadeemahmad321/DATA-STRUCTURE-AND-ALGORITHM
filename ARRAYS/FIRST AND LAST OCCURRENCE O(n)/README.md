# First and Last Occurrence Finder

This C++ program finds the first and last occurrence of a specified key element in an array. It efficiently traverses the array in a single pass, achieving a time complexity of O(n).

## Features

- Prompts the user to input the size and elements of an array.
- Allows the user to specify a key element to search for.
- Outputs the indices of the first and last occurrences of the key.
- Handles the case where the key is not found in the array.

## Getting Started

### Prerequisites

Make sure you have a C++ compiler installed on your system. You can use g++, clang++, or any IDE that supports C++ development.

### Compilation

To compile the program, use the following command:

```bash
g++ -o find_occurrences find_occurrences.cpp
```

### Usage

Run the compiled program:

```bash
./find_occurrences
```

Follow the prompts to enter the size of the array, the elements, and the key element you want to search for.

## Example

Here is an example of how the program works:

```
Enter the size of the array: 7
Enter the elements of the array: 1 2 3 2 4 5 2
Enter the key element: 2
```

### Step-by-Step Explanation

1. **Input Size**: The user is prompted to enter the size of the array:
   - User enters `7`.

2. **Input Elements**: The user is prompted to enter the elements of the array:
   - User enters: `1 2 3 2 4 5 2`.
   - The resulting array is: `[1, 2, 3, 2, 4, 5, 2]`.

3. **Key Element**: The user specifies the key element to search for:
   - User enters `2`.

4. **Finding Occurrences**:
   - The program initializes `first` and `last` to `-1`.
   - It iterates through the array:
     - **Index 0**: Value `1` (not equal to `2`), continue.
     - **Index 1**: Value `2` (equal to `2`):
       - Set `first` to `1` (first occurrence found).
       - Set `last` to `1` (last occurrence so far).
     - **Index 2**: Value `3` (not equal to `2`), continue.
     - **Index 3**: Value `2` (equal to `2`):
       - Update `last` to `3`.
     - **Index 4**: Value `4` (not equal to `2`), continue.
     - **Index 5**: Value `5` (not equal to `2`), continue.
     - **Index 6**: Value `2` (equal to `2`):
       - Update `last` to `6`.
   
5. **Final Output**:
   - After the loop, `first` is `1` and `last` is `6`.
   - The output will be:
   ```
   First occurrence: 1
   Last occurrence: 6
   ```

If the user enters a key that is not present in the array, such as `9`, the output would be:
```
Element not found in the array.
```

## Complexity

- **Time Complexity**: O(n), where n is the number of elements in the array. The program makes a single pass through the array to find the first and last occurrences of the key.
- **Space Complexity**: O(1), as no additional data structures are used that scale with input size. The algorithm only uses a fixed number of variables.

## Important Information

- The program assumes valid input for size and array elements.
- Make sure to test with different arrays and keys to ensure robustness.
