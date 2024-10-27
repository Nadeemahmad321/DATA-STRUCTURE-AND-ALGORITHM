# Sum of Digits Program

This C++ program calculates the sum of the digits of a given integer. It prompts the user to enter a number and then computes the sum of its individual digits. 

## Table of Contents

- [Features](#features)
- [Requirements](#requirements)
- [How It Works](#how-it-works)
- [Usage](#usage)
- [Example](#example)

## Features

- Simple user interface to input a number.
- Computes the sum of the digits efficiently.
- Displays the result clearly.

## Requirements

- A C++ compiler (e.g., g++, clang++).
- Basic knowledge of how to compile and run C++ programs.

## How It Works

1. **Function Definition**: The program defines a function `sumOfDigit(int n)` that takes an integer as an argument.
2. **Digit Extraction**: Inside the function, a loop is used to repeatedly extract the last digit of the number using the modulus operator (`%`) and adds it to a sum variable.
3. **Updating the Number**: After extracting the last digit, the program divides the number by 10 (`n /= 10`), effectively removing that last digit.
4. **Looping**: This process continues until the number is reduced to zero.
5. **Returning the Result**: Finally, the function returns the computed sum of the digits.
6. **User Interaction**: In the `main` function, the program prompts the user to enter a number, calls the `sumOfDigit` function, and prints the result.

## Usage

1. **Clone the repository or download the code file**:

   ```bash
   git clone https://github.com/yourusername/sum-of-digits.git
   ```

2. **Navigate to the directory**:

   ```bash
   cd sum-of-digits
   ```

3. **Compile the code**:

   ```bash
   g++ -o sum_of_digits sum_of_digits.cpp
   ```

4. **Run the program**:

   ```bash
   ./sum_of_digits
   ```

5. **Input**: When prompted, enter an integer number.

6. **Output**: The program will display the sum of the digits of the entered number.

## Example

### Input and Output

```
Enter the number: 12345
Sum of its digits is: 15
```

### Explanation

- **Input**: The user inputs `12345`.
- **Process**:
  - The last digit `5` is extracted, and `sum` becomes `5`.
  - The next digit `4` is extracted, and `sum` becomes `9` (`5 + 4`).
  - The next digit `3` is extracted, and `sum` becomes `12` (`9 + 3`).
  - The next digit `2` is extracted, and `sum` becomes `14` (`12 + 2`).
  - The last digit `1` is extracted, and `sum` becomes `15` (`14 + 1`).
- **Output**: The program then displays `Sum of its digits is: 15`.
