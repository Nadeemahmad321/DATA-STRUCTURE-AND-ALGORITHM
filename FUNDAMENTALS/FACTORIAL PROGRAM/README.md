# Factorial Program in C++

## Description

This C++ program calculates the factorial of a given non-negative integer using a while loop. The factorial of a number \( n \) (denoted as \( n! \)) is the product of all positive integers from 1 to \( n \). The program handles invalid inputs by prompting the user to enter a valid number.

## Features

- Computes the factorial of non-negative integers.
- Handles input validation for negative numbers.
- Utilizes a while loop for the calculation.

## Usage

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/factorial-program.git
   cd factorial-program
   ```

2. **Compile the Program**
   Use a C++ compiler like `g++`:
   ```bash
   g++ factorial.cpp -o factorial
   ```

3. **Run the Program**
   ```bash
   ./factorial
   ```

4. **Input**
   - Enter a non-negative integer when prompted.

5. **Output**
   - The program will display the factorial of the entered number or an error message if the input is invalid.

## Example

### Input
```
Enter the number: 5
```

### Explanation
When you enter `5`, the program calculates the factorial \( 5! \) as follows:

- **Initialization:** 
  - `fact` is initialized to `1`.
  - `i` is initialized to `1`.

- **While Loop Execution:**
  - Iteration 1: \( i = 1 \) → \( fact = 1 \times 1 = 1 \) → Increment \( i \) to `2`
  - Iteration 2: \( i = 2 \) → \( fact = 1 \times 2 = 2 \) → Increment \( i \) to `3`
  - Iteration 3: \( i = 3 \) → \( fact = 2 \times 3 = 6 \) → Increment \( i \) to `4`
  - Iteration 4: \( i = 4 \) → \( fact = 6 \times 4 = 24 \) → Increment \( i \) to `5`
  - Iteration 5: \( i = 5 \) → \( fact = 24 \times 5 = 120 \) → Increment \( i \) to `6`

- **Loop Termination:** The loop stops as \( i \) becomes `6`, which is greater than `5`.

### Output
```
Factorial of 5 is: 120
```

### Another Example

#### Input
```
Enter the number: -3
```

#### Explanation
When you enter `-3`, the program checks if the input is valid. Since `-3` is a negative number, the program does not attempt to calculate the factorial.

### Output
```
Please enter a number that is greater than or equal to 0!
```

## Code Structure

- `factorial(int n)`: Computes the factorial of `n` using a while loop.
- `main()`: Handles user input and displays results.

## Requirements

- C++ Compiler (g++, clang++, etc.)
- Basic understanding of C++ syntax
