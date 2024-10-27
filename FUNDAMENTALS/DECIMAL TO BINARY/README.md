# Decimal to Binary Converter

This C++ program converts a decimal number to its binary representation.

## Description

The program prompts the user to enter a decimal number and then converts that number to binary. It uses bitwise operations and the `pow` function to calculate the binary equivalent and displays the result.

## Features

- User-friendly input and output.
- Efficient conversion using bitwise operations.
- Displays the binary representation as a number.

## How It Works

1. **Input**: The user is asked to input a decimal number.
2. **Conversion Process**:
   - The program repeatedly extracts the least significant bit (LSB) of the number using bitwise AND (`&`).
   - It calculates the positional value of the bit using `pow(10, i)` where `i` is the current bit position.
   - The number is right-shifted (`>>`) to process the next bit.
   - This process continues until the number becomes zero.
3. **Output**: The final binary representation is constructed and displayed.

## Code Overview

```cpp
#include<iostream>
#include<cmath> // Include cmath for pow
using namespace std;

int decimalToBinary(int n) {
    int ans = 0; // Variable to store the binary result
    int i = 0;   // Position counter
    while (n != 0) { // Loop until all bits are processed
        int bit = n & 1; // Get the least significant bit
        ans += bit * pow(10, i); // Add the bit to the result at the correct position
        n = n >> 1; // Right shift to process the next bit
        i++; // Move to the next position
    }
    return ans; // Return the final binary result
}

int main() {
    int n;
    cout << "Enter the number: ";
    cin >> n; // Input from the user
    int ans = decimalToBinary(n); // Call the conversion function
    cout << "Binary representation: " << ans << endl; // Display the result
    return 0; // Exit the program
}
```

## Example

Let's go through an example step-by-step.

### Input

Assume the user enters the decimal number `13`.

### Conversion Steps

1. **Initial Value**:
   - `n = 13`
   - `ans = 0`, `i = 0`
   
2. **First Iteration**:
   - Calculate the LSB: `bit = 13 & 1 = 1`
   - Update `ans`: `ans += 1 * pow(10, 0) = 0 + 1 = 1`
   - Right shift `n`: `n = 13 >> 1 = 6`
   - Increment `i`: `i = 1`

3. **Second Iteration**:
   - `n = 6`
   - Calculate the LSB: `bit = 6 & 1 = 0`
   - Update `ans`: `ans += 0 * pow(10, 1) = 1 + 0 = 1`
   - Right shift `n`: `n = 6 >> 1 = 3`
   - Increment `i`: `i = 2`

4. **Third Iteration**:
   - `n = 3`
   - Calculate the LSB: `bit = 3 & 1 = 1`
   - Update `ans`: `ans += 1 * pow(10, 2) = 1 + 100 = 101`
   - Right shift `n`: `n = 3 >> 1 = 1`
   - Increment `i`: `i = 3`

5. **Fourth Iteration**:
   - `n = 1`
   - Calculate the LSB: `bit = 1 & 1 = 1`
   - Update `ans`: `ans += 1 * pow(10, 3) = 101 + 1000 = 1101`
   - Right shift `n`: `n = 1 >> 1 = 0`
   - Increment `i`: `i = 4`

6. **Exit Loop**: Since `n` is now `0`, the loop exits.

### Final Output

The final value of `ans` is `1101`, which is the binary representation of the decimal number `13`.

```
Binary representation: 1101
```

## Compilation and Execution

To compile and run this program, follow these steps:

1. Ensure you have a C++ compiler installed (like g++ or clang).
2. Save the code to a file named `decimal_to_binary.cpp`.
3. Open a terminal and navigate to the directory where the file is saved.
4. Compile the program:
   ```bash
   g++ decimal_to_binary.cpp -o decimal_to_binary
   ```
5. Run the executable:
   ```bash
   ./decimal_to_binary
   ```

## Notes

- The program outputs the binary representation as a decimal number. For example, the binary representation of `5` is displayed as `101`.
- Ensure to enter a non-negative integer as input for proper conversion.
