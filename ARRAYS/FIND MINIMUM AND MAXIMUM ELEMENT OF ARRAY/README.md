# Find Minimum and Maximum Element of an Array

This C++ program allows users to input an array of integers and finds both the minimum and maximum elements within that array. It includes functions for traversing the array and printing its elements, as well as for finding the minimum and maximum values.

## Features

- Input validation for the array size.
- Functions to traverse and print the array.
- Functions to find the minimum and maximum elements in the array.

## Requirements

- A C++ compiler (e.g., g++, clang++).
- Basic understanding of C++ syntax and functions.

## Usage

1. **Compile the Program**  
   Use a C++ compiler to compile the program. For example, using g++:
   ```bash
   g++ -o find_min_max find_min_max.cpp
   ```

2. **Run the Program**  
   Execute the compiled program:
   ```bash
   ./find_min_max
   ```

3. **Input**  
   - Enter the size of the array (between 1 and 100).
   - Input the elements of the array.

4. **Output**  
   - The program will display the elements of the array.
   - It will then display the minimum and maximum elements found in the array.

## Example

### Input

```
Enter the size of the array: 5
Enter the elements of the array:
12
3
7
19
5
```

### Output

```
Elements of the array: 12 3 7 19 5 
Minimum element of array: 3
Maximum element of array: 19
```

### Explanation

1. **Input Size**: The user first inputs the size of the array, which in this case is `5`.
2. **Input Elements**: The user then inputs the elements of the array: `12`, `3`, `7`, `19`, and `5`.
3. **Array Traversal**: The program prints the elements of the array.
4. **Finding Minimum**: The function for finding the minimum value iterates through the array and identifies `3` as the minimum.
5. **Finding Maximum**: The function for finding the maximum value iterates through the array and identifies `19` as the maximum.

## Complexity Analysis

- **Time Complexity**:  
  - Traversing the array takes O(n) time, where n is the number of elements in the array.
  - Finding the minimum and maximum also takes O(n) time each.
  - Overall, the time complexity of the program is O(n).

- **Space Complexity**:  
  - The space complexity is O(1) since the algorithm uses a fixed amount of extra space (for the min and max variables) regardless of the input size.

## Important Information

- **Input Validation**: The program checks if the input size is valid (between 1 and 100) and prompts the user accordingly.
- **Data Type**: The program assumes that all input values are integers.
- **Extensibility**: This program can be extended to handle larger arrays or different data types (e.g., floating-point numbers) with minor modifications.
