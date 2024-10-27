# Binary to Decimal Converter

This C++ program converts a binary number (input as an integer) into its decimal representation. It reads the binary number from the user and outputs the corresponding decimal value.

## Features

- Converts binary numbers (e.g., `1011`) to decimal (e.g., `11`).
- Simple and user-friendly interface for input and output.
- Uses basic mathematical operations to perform the conversion.

## How It Works

1. The user is prompted to enter a binary number.
2. The program processes each digit of the binary number:
   - If the digit is `1`, it adds the corresponding power of `2` based on the digit's position.
3. The decimal value is then displayed as the output.

## Code Explanation

### Key Components

- **binaryToDecimal(int n)**: 
  - This function takes a binary number as an integer and converts it to its decimal equivalent.
  - It processes each digit from right to left, accumulating the decimal result.

- **main()**:
  - The entry point of the program.
  - Handles user interaction: prompting for input, calling the conversion function, and displaying the output.

### Example

Let's walk through an example to illustrate how the conversion works.

#### Input
Suppose the user inputs the binary number `1011`.

#### Conversion Process
The binary number `1011` can be broken down as follows:

- **Positioning** (right to left):
  - `1` (position 3, \(2^3\))
  - `0` (position 2, \(2^2\))
  - `1` (position 1, \(2^1\))
  - `1` (position 0, \(2^0\))

#### Calculation Steps
1. **Initialize**:
   - `ans = 0` (to hold the decimal result)
   - `i = 0` (to track the current position)

2. **Process Each Digit**:
   - **Digit = 1** (position 0):
     - Since the digit is `1`, add \(2^0 = 1\) to `ans`.
     - New `ans = 0 + 1 = 1`
     - Increment `i` to `1`.
   - **Digit = 1** (position 1):
     - The digit is `1`, add \(2^1 = 2\) to `ans`.
     - New `ans = 1 + 2 = 3`
     - Increment `i` to `2`.
   - **Digit = 0** (position 2):
     - The digit is `0`, so `ans` remains `3`.
     - Increment `i` to `3`.
   - **Digit = 1** (position 3):
     - The digit is `1`, add \(2^3 = 8\) to `ans`.
     - New `ans = 3 + 8 = 11`
     - Increment `i` to `4`.

3. **Final Result**:
   - The loop ends when there are no more digits.
   - The final value of `ans` is `11`.

#### Output
The program will display:
```
Decimal representation: 11
```

## Prerequisites

- A C++ compiler (e.g., g++, clang++)
- Basic understanding of C++ syntax and concepts

## How to Run the Program

1. Clone the repository or download the source code.
2. Open a terminal and navigate to the directory containing the code.
3. Compile the code using:
   ```bash
   g++ -o binary_to_decimal binary_to_decimal.cpp
   ```
4. Run the compiled program:
   ```bash
   ./binary_to_decimal
   ```
5. Enter a binary number when prompted.

