# nCr Calculator

This program calculates the number of combinations (nCr) for given values of `n` and `r`, where `n` is the total number of items and `r` is the number of items to choose. The formula for combinations is given by:

\[ nCr = \frac{n!}{r!(n - r)!} \]

where `!` denotes factorial, the product of all positive integers up to that number.

## Features

- Calculates factorial of a number.
- Computes combinations using the nCr formula.
- Validates input to ensure `n` and `r` are non-negative integers.
- Handles edge cases where `r` is greater than `n` or negative.

## How to Use

1. Compile the program using a C++ compiler.
2. Run the compiled program.
3. Input the values for `n` and `r` when prompted.
4. The program will output the calculated value of nCr.

### Example

Let's say we want to calculate \( 5C3 \):

1. **Input**:
   - Enter `n`: `5`
   - Enter `r`: `3`

2. **Calculation**:
   - First, compute the factorial of `5`:  
     \( 5! = 5 \times 4 \times 3 \times 2 \times 1 = 120 \)
   - Next, compute the factorial of `3`:  
     \( 3! = 3 \times 2 \times 1 = 6 \)
   - Then, compute the factorial of `2` (which is \( 5 - 3 \)):  
     \( 2! = 2 \times 1 = 2 \)
   - Now, apply the nCr formula:  
     \( 5C3 = \frac{5!}{3!(5 - 3)!} = \frac{120}{6 \times 2} = \frac{120}{12} = 10 \)

3. **Output**:
   - The program will display:  
     `nCr(5, 3) = 10`

## Code Explanation

### Functions

- **factorial(int x)**: Computes the factorial of a given integer `x`. If `x` is negative, it returns `-1` to indicate an invalid input.

- **nCr(int n, int r)**: Calculates the combinations of `n` items taken `r` at a time. It checks for valid values of `r` (must be between `0` and `n`). It uses the factorial function to compute the result and handles cases where the denominator might be zero.

### Main Function

The `main` function handles user input, validates it, and calls the `nCr` function to compute the result. It ensures that both `n` and `r` are non-negative integers and displays the result in a clear format.

## Requirements

- A C++ compiler (e.g., g++, clang++)
- Basic understanding of C++ programming
