# Reverse Integer

This program reverses the digits of a given integer. It takes an integer as input and outputs its reverse. If the reversed integer overflows the limits of a 32-bit signed integer, the function returns 0.

## Features

- Accepts a signed integer input from the user.
- Reverses the digits of the integer.
- Handles overflow conditions for 32-bit signed integers.

## Code Explanation

### Header and Namespace

```cpp
#include <iostream>
using namespace std;
```

- **`#include <iostream>`**: Includes the Input/Output stream library, which allows us to use `cin` and `cout` for input and output operations.
- **`using namespace std;`**: This line allows us to use standard functions and objects like `cin` and `cout` without needing to prefix them with `std::`.

### Function Definition

```cpp
int reverseInteger(int n) {
    int ans = 0; // Variable to hold the reversed number
```

- **`reverseInteger(int n)`**: This function takes an integer `n` as input and returns its reversed form.
- **`int ans = 0;`**: Initializes a variable `ans` to store the reversed integer.

### Looping through Digits

```cpp
while (n != 0) {
    int digit = n % 10; // Get the last digit of n
```

- **`while (n != 0)`**: This loop continues until all digits of `n` have been processed.
- **`int digit = n % 10;`**: Extracts the last digit of `n` using the modulus operator. For example, if `n` is 123, `digit` becomes 3.

### Overflow Check

```cpp
if (ans > INT_MAX / 10 || ans < INT_MIN / 10) {
    return 0; // Return 0 if overflow occurs
}
```

- Before updating `ans`, we check if multiplying `ans` by 10 would cause it to exceed the maximum or minimum value for a 32-bit signed integer.
  - **`INT_MAX / 10`**: The maximum value for a signed integer divided by 10. If `ans` is greater than this, multiplying by 10 will overflow.
  - **`INT_MIN / 10`**: The minimum value for a signed integer divided by 10. If `ans` is less than this, it indicates a potential underflow.

### Building the Reversed Number

```cpp
ans = (ans * 10) + digit; // Build the reversed number
n /= 10; // Remove the last digit from n
```

- **`ans = (ans * 10) + digit;`**: Shifts the existing digits in `ans` to the left (by multiplying by 10) and adds the new last digit.
- **`n /= 10;`**: Removes the last digit from `n` by performing integer division.

### Returning the Result

```cpp
return ans; // Return the reversed integer
```

- After all digits have been processed, the function returns the reversed integer.

### Main Function

```cpp
int main() {
    int n;
    cout << "Enter the number: "; // Prompt user for input
    cin >> n; // Read integer input

    int reverse = reverseInteger(n); // Call function to reverse the integer
    cout << "Reverse: " << reverse; // Display the reversed integer
    return 0; // Exit program
}
```

- **`int main()`**: The entry point of the program.
- **`cout << "Enter the number: ";`**: Prompts the user to input a number.
- **`cin >> n;`**: Reads the integer value entered by the user.
- **`int reverse = reverseInteger(n);`**: Calls the `reverseInteger` function with the user-provided input and stores the result.
- **`cout << "Reverse: " << reverse;`**: Outputs the reversed integer.
- **`return 0;`**: Indicates successful completion of the program.

## Usage

1. Compile the program using a C++ compiler.
   ```bash
   g++ reverse_integer.cpp -o reverse_integer
   ```
   Replace `reverse_integer.cpp` with the filename you saved the code as.
   
2. Run the executable.
   ```bash
   ./reverse_integer
   ```
   
3. Enter an integer when prompted.
4. View the reversed integer output.

## Limitations

- The program only handles 32-bit signed integers.
- If the reversed integer exceeds the bounds of a 32-bit signed integer, it returns 0 instead of the reversed value.

## Compilation

To compile the program, use the following command:

```bash
g++ reverse_integer.cpp -o reverse_integer
```
