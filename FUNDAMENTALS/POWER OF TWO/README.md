# Power of Two Checker

This C++ program checks whether a given integer is a power of two. A number is a power of two if it can be expressed as \(2^n\) where \(n\) is a non-negative integer.

## Features

- Prompts the user to input an integer.
- Determines if the input number is a power of two.
- Outputs `True` if it is a power of two; otherwise, it outputs `False`.

## Code Explanation

The code consists of the following components:

1. **Header Files**:
   - `#include <iostream>`: Enables input and output operations.
   - `#include <cmath>`: Provides access to mathematical functions.

2. **Function: `isPower(int n)`**:
   - This function checks if the integer `n` is a power of two.
   - It initializes `ans` to `1` (which is \(2^0\)).
   - A loop iterates through possible powers of two (up to \(2^{30}\)):
     - If `ans` equals `n`, the function returns `true`, indicating `n` is a power of two.
     - Before multiplying `ans` by `2`, it checks for potential overflow by ensuring `ans < INT_MAX / 2`.
   - If no power of two matches `n`, the function returns `false`.

3. **Main Function**:
   - Prompts the user to enter a number.
   - Calls the `isPower` function to check if the number is a power of two.
   - Prints the result to the console.

## Example Usage

Let's go through an example where the user inputs the number `16`.

### Example

1. **Input**: 
   ```
   Enter the number: 16
   ```

2. **Execution Flow**:
   - The program begins by calling the `isPower(16)` function.
   - Inside `isPower`, `ans` is initialized to `1` (which is \(2^0\)).
   - The loop starts:
     - **Iteration 0**: `ans = 1` (not equal to `16`), updates `ans` to `2`.
     - **Iteration 1**: `ans = 2` (not equal to `16`), updates `ans` to `4`.
     - **Iteration 2**: `ans = 4` (not equal to `16`), updates `ans` to `8`.
     - **Iteration 3**: `ans = 8` (not equal to `16`), updates `ans` to `16`.
     - **Iteration 4**: `ans = 16` (equal to `16`), returns `true`.

3. **Output**: 
   ```
   True
   ```

### Explanation

- The input `16` is a power of two because it can be expressed as \(2^4\).
- The loop iteratively calculates powers of two, comparing each result with `n` (which is `16`).
- When the loop reaches \(2^4\), it finds a match, thus confirming that `16` is indeed a power of two.

## How to Compile and Run

To compile and run this program, follow these steps:

1. Ensure you have a C++ compiler installed (e.g., g++, clang++).
2. Save the code to a file named `power_of_two.cpp`.
3. Open a terminal and navigate to the directory where the file is saved.
4. Compile the program using the command:
   ```bash
   g++ -o power_of_two power_of_two.cpp
   ```
5. Run the compiled program:
   ```bash
   ./power_of_two
   ```

## Limitations

- The program currently handles positive integers. Negative numbers and zero are not considered powers of two in this implementation.
- The function checks powers of two up to \(2^{30}\), which may not be sufficient for very large values of `n`.
