# Mini Calculator

A simple console-based calculator program implemented in C++. This program allows users to perform basic arithmetic operations, including addition, subtraction, multiplication, division, and modulus.

## Features

- Supports the following operations:
  - Addition (`+`)
  - Subtraction (`-`)
  - Multiplication (`*`)
  - Division (`/`)
  - Modulus (`%`)
- Handles division by zero with error messages.
- Allows continuous calculations until the user decides to exit.

## Prerequisites

- A C++ compiler (e.g., g++, clang++).
- Basic understanding of C++ programming.

## How to Compile and Run

1. **Clone the repository** (if applicable):
   ```bash
   git clone <repository-url>
   cd mini-calculator
   ```

2. **Compile the program**:
   ```bash
   g++ mini_calculator.cpp -o mini_calculator
   ```

3. **Run the program**:
   ```bash
   ./mini_calculator
   ```

## Usage

1. Start the program.
2. Input the first number when prompted.
3. Input the desired operator (`+`, `-`, `*`, `/`, `%`).
4. Input the second number.
5. The result will be displayed.
6. You will be prompted to perform another calculation or exit the program.

## Example

### Step-by-Step Explanation

**Input Sequence:**

```
Enter the first number: 25
Enter the operator (+ - * / %): /
Enter the second number: 5
```

**Output:**

```
Result: 5
Do you want to perform another calculation? (y/n): y
```

### Breakdown of the Example

1. **Entering the First Number:**
   - The user is prompted to enter the first number. In this case, the user inputs `25`.

2. **Choosing an Operator:**
   - The program asks for an operator. The user selects the division operator (`/`).

3. **Entering the Second Number:**
   - The user is prompted for the second number, and inputs `5`.

4. **Calculation:**
   - The program calculates the result of `25 / 5`, which is `5`.

5. **Displaying the Result:**
   - The program outputs `Result: 5`.

6. **Continuation:**
   - The user is asked if they want to perform another calculation. The user inputs `y` to continue.

### Additional Example with Division by Zero

**Input Sequence:**

```
Enter the first number: 18
Enter the operator (+ - * / %): /
Enter the second number: 0
```

**Output:**

```
Error: Division by zero!
Do you want to perform another calculation? (y/n): n
```

#### Explanation of the Additional Example

1. **Entering the First Number:**
   - The user enters `18` as the first number.

2. **Choosing an Operator:**
   - The user selects the division operator (`/`).

3. **Entering the Second Number:**
   - The user inputs `0` as the second number.

4. **Error Handling:**
   - Since division by zero is not allowed, the program checks the second number before performing the division. It outputs the error message: `Error: Division by zero!`.

5. **Continuation:**
   - The user is prompted to decide whether to perform another calculation. The user inputs `n` to exit the program.
