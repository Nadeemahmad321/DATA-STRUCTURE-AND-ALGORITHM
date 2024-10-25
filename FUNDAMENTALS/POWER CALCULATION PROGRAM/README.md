# Power Calculation Program

This C++ program calculates the power of a given base raised to a non-negative exponent using an iterative approach. It serves as a straightforward example of basic input/output, control structures, and functions in C++.

## Features

- Prompts the user to enter a base and a non-negative exponent.
- Validates the input to ensure the exponent is non-negative.
- Computes the power using a loop.
- Displays the result in a clear, readable format.

## Requirements

- A C++ compiler (e.g., g++, clang++)
- Basic understanding of C++ syntax and concepts

## Code Overview

Here’s the complete code for the program:

```cpp
#include <iostream>
using namespace std;

int powerOfNumber(int base, int exponent) {
    int result = 1;
    for (int i = 0; i < exponent; i++) {
        result *= base;
    }
    return result;
}

int main() {
    int base, exponent;
    cout << "Enter the base: ";
    cin >> base;
    cout << "Enter the exponent (non-negative): ";
    cin >> exponent;

    // Ensure the exponent is non-negative
    if (exponent < 0) {
        cout << "Exponent must be non-negative." << endl;
        return 1;
    }

    int pow = powerOfNumber(base, exponent);
    cout << base << "^" << exponent << " = " << pow << endl;

    return 0;
}
```

### Explanation of the Code

1. **Header Inclusion**:
   ```cpp
   #include <iostream>
   using namespace std;
   ```
   - This includes the input-output stream library to enable the program to read from standard input and write to standard output.

2. **Function Declaration**:
   ```cpp
   int powerOfNumber(int base, int exponent) {
       int result = 1;
       for (int i = 0; i < exponent; i++) {
           result *= base;
       }
       return result;
   }
   ```
   - This function calculates the power of a number.
   - It initializes a variable `result` to 1.
   - It then uses a loop to multiply `result` by `base` for the number of times specified by `exponent`.

3. **Main Function**:
   ```cpp
   int main() {
       int base, exponent;
       cout << "Enter the base: ";
       cin >> base;
       cout << "Enter the exponent (non-negative): ";
       cin >> exponent;
   ```
   - The `main` function starts the program execution.
   - It declares two integer variables, `base` and `exponent`, to store user input.

4. **Input Validation**:
   ```cpp
   if (exponent < 0) {
       cout << "Exponent must be non-negative." << endl;
       return 1;
   }
   ```
   - The program checks if the entered exponent is negative.
   - If it is, an error message is displayed, and the program exits with a return code of `1`.

5. **Calling the Function**:
   ```cpp
   int pow = powerOfNumber(base, exponent);
   cout << base << "^" << exponent << " = " << pow << endl;
   ```
   - The `powerOfNumber` function is called with the user-provided `base` and `exponent`.
   - The result is stored in the variable `pow` and printed to the console.

6. **Program Termination**:
   ```cpp
   return 0;
   ```
   - The program returns `0`, indicating successful execution.

## Usage

1. **Clone or Download the Repository**: Obtain the source code by cloning the repository or downloading the file.
   
2. **Compile the Program**: Use a C++ compiler like g++:
   ```bash
   g++ power_calculation.cpp -o power_calculation
   ```

3. **Run the Compiled Program**:
   ```bash
   ./power_calculation
   ```

4. **Follow the Prompts**: Enter the base and the exponent when prompted.

## Example Interaction

```
Enter the base: 2
Enter the exponent (non-negative): 3
2^3 = 8
```

## Error Handling

- The program validates that the exponent is non-negative. If the user enters a negative exponent, it displays an error message and terminates.

