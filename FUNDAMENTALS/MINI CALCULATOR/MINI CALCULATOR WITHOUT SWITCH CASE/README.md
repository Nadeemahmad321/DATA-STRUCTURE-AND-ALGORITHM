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
Enter the first number: 12
Enter the operator (+ - * / %): *
Enter the second number: 4
```

**Output:**

```
Result: 48
Do you want to perform another calculation? (y/n): y
```

### Breakdown of the Example

1. **Entering the First Number:**
   - The user is prompted to enter the first number. In this case, the user inputs `12`.

2. **Choosing an Operator:**
   - The program asks for an operator. The user selects the multiplication operator (`*`).

3. **Entering the Second Number:**
   - The user is prompted again, this time for the second number, and inputs `4`.

4. **Calculation:**
   - The program calculates the result of `12 * 4`, which is `48`.

5. **Displaying the Result:**
   - The program outputs `Result: 48`.

6. **Continuation:**
   - The user is asked if they want to perform another calculation. The user inputs `y` to continue.

### Additional Example

**Input Sequence:**

```
Enter the first number: 15
Enter the operator (+ - * / %): /
Enter the second number: 0
```

**Output:**

```
Error: Division by zero!
Do you want to perform another calculation? (y/n): n
```

#### Explanation of the Additional Example

1. The user enters `15` as the first number.
2. The user selects the division operator (`/`).
3. The user enters `0` as the second number.
4. Since division by zero is not allowed, the program outputs an error message: `Error: Division by zero!`.
5. The user is again prompted to continue or exit.
