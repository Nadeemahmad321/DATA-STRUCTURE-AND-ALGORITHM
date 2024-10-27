# Odd or Even Number Checker

This C++ program checks whether a given integer is odd or even. It prompts the user to enter a number and provides the result based on the input.

## Features

- Simple and interactive user interface.
- Checks if the number is odd or even.
- Returns clear and descriptive output.

## How It Works

1. The program defines a function `oddEven` that takes an integer as an argument and returns `true` if the number is odd and `false` if it is even.
2. In the `main` function, the program prompts the user to enter a number.
3. It calls the `oddEven` function and displays whether the number is odd or even.

## Prerequisites

- A C++ compiler (e.g., g++, clang++)
- Basic understanding of C++ programming.

## Compilation and Execution

To compile and run the program, follow these steps:

1. Save the code to a file named `odd_even_checker.cpp`.
2. Open a terminal and navigate to the directory where the file is saved.
3. Compile the program using the following command:
   ```bash
   g++ -o odd_even_checker odd_even_checker.cpp
   ```
4. Run the compiled program:
   ```bash
   ./odd_even_checker
   ```

## Example

### Input and Output

1. **Example 1: Checking an Odd Number**
   ```
   Enter a number: 5
   The number 5 is odd.
   ```

   **Explanation**:
   - The user is prompted to enter a number.
   - The user enters `5`.
   - The program calls the `oddEven` function with `5` as an argument.
   - Inside `oddEven`, the expression `5 % 2` evaluates to `1` (since 5 divided by 2 leaves a remainder of 1).
   - Therefore, `5 % 2 != 0` evaluates to `true`, indicating that `5` is odd.
   - The program outputs: "The number 5 is odd."

2. **Example 2: Checking an Even Number**
   ```
   Enter a number: 10
   The number 10 is even.
   ```

   **Explanation**:
   - The user is prompted to enter a number.
   - The user enters `10`.
   - The program calls the `oddEven` function with `10` as an argument.
   - Inside `oddEven`, the expression `10 % 2` evaluates to `0` (since 10 divided by 2 leaves no remainder).
   - Therefore, `10 % 2 != 0` evaluates to `false`, indicating that `10` is even.
   - The program outputs: "The number 10 is even."

## Conclusion

This program provides a straightforward way to determine if a number is odd or even. It serves as a basic introduction to functions and user input in C++. You can enhance this program by adding more features, such as error handling or the ability to check multiple numbers at once.
