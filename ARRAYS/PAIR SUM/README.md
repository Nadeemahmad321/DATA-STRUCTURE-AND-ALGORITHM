# Pair Sum Finder

This program finds and prints all unique pairs of elements in an array that sum up to a specified target value.

## Features

- Takes user input for the size of the array and its elements.
- Prompts for a target sum.
- Outputs all pairs of elements whose sum equals the target.

## How It Works

1. **User Input**:
   - The user is prompted to enter the size of the array.
   - The user inputs the elements of the array.
   - The user specifies a target sum.

2. **Finding Pairs**:
   - The program checks all possible pairs of elements in the array.
   - For each pair, it checks if their sum matches the target sum.

3. **Output**:
   - It prints the pairs that meet the criteria in sorted order.

## Example

### Input/Output Example

```
Enter the size of array: 5
Enter the elements of array: 1 2 3 4 5
Enter the target: 5
Pair sums are: (1, 4)(2, 3)
```

### Explanation of the Example

1. **Input**:
   - The user specifies the size of the array as `5`.
   - The user inputs the elements: `1, 2, 3, 4, 5`.
   - The target sum provided by the user is `5`.

2. **Processing**:
   - The program evaluates the pairs of elements:
     - (1, 2) → Sum = 3 (not a match)
     - (1, 3) → Sum = 4 (not a match)
     - (1, 4) → Sum = 5 (match found)
     - (1, 5) → Sum = 6 (not a match)
     - (2, 3) → Sum = 5 (match found)
     - (2, 4) → Sum = 6 (not a match)
     - (2, 5) → Sum = 7 (not a match)
     - (3, 4) → Sum = 7 (not a match)
     - (3, 5) → Sum = 8 (not a match)
     - (4, 5) → Sum = 9 (not a match)

3. **Output**:
   - The program prints the pairs that sum to `5`: `(1, 4)` and `(2, 3)`.

## Complexity Analysis

- **Time Complexity**: O(n²)
  - The program uses a nested loop to evaluate pairs, leading to quadratic complexity, where `n` is the number of elements in the array.

- **Space Complexity**: O(1)
  - The algorithm does not use any additional data structures that scale with input size, maintaining constant space usage.

## Important Information

- Ensure that the input array size does not exceed the predefined limit (in this case, `100`).
- This program only considers unique pairs; each pair is printed once.
- The pairs are printed in sorted order based on their values.

## Compilation and Execution

To compile and run the program, follow these steps:

1. Save the code in a file named `pair_sum.cpp`.
2. Open a terminal and navigate to the directory containing the file.
3. Compile the code using a C++ compiler, for example:
   ```bash
   g++ pair_sum.cpp -o pair_sum
   ```
4. Run the compiled program:
   ```bash
   ./pair_sum
   ```
