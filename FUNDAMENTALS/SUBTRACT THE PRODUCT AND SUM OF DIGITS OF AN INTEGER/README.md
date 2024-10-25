# Subtract the Product and Sum of Digits of an Integer

## Description
This C++ program calculates the sum and product of the digits of an integer input by the user. It then subtracts the sum from the product and displays the result. The program is straightforward and serves as a practical example of basic arithmetic operations, loops, and user input in C++.

## Features
- **User Input**: Prompts the user to enter a non-negative integer.
- **Digit Calculation**: Computes both the sum and product of the digits.
- **Output**: Displays the sum, product, and the result of the subtraction of the sum from the product.

## Requirements
- A C++ compiler (such as `g++` or `clang++`).
- Basic understanding of running C++ programs.

## Code Explanation

### Header and Namespace
```cpp
#include<iostream>
using namespace std;
```
- `#include<iostream>`: This directive includes the Input/Output stream library, which is necessary for using `cin` and `cout`.
- `using namespace std;`: This statement allows us to use standard library names without the `std::` prefix.

### Main Function
```cpp
int main() {
```
- This is the entry point of the program.

### Variable Declaration
```cpp
int num;
```
- `num`: This variable will store the integer input from the user.

### User Input
```cpp
cout << "Enter a number: ";
cin >> num;
```
- The program prompts the user to enter a number and stores it in `num`.

### Initialize Sum and Product
```cpp
int sum = 0;
int prod = 1;
```
- `sum`: Initialized to 0 to accumulate the sum of the digits.
- `prod`: Initialized to 1 because multiplying by 1 does not affect the product.

### While Loop for Digit Calculation
```cpp
while(num != 0) {
    int digit = num % 10;
    sum += digit;
    prod *= digit;
    num /= 10;
}
```
- The loop continues until `num` becomes 0.
- `int digit = num % 10;`: Extracts the last digit of `num`.
- `sum += digit;`: Adds the extracted digit to `sum`.
- `prod *= digit;`: Multiplies the extracted digit to `prod`.
- `num /= 10;`: Removes the last digit from `num`.

### Output Results
```cpp
cout << "Sum of its digits is: " << sum << endl;
cout << "Product of its digits is: " << prod << endl;
cout << "After subtraction (Product - Sum): " << (prod - sum) << endl;
```
- Displays the sum of the digits.
- Displays the product of the digits.
- Displays the result of subtracting the sum from the product.

### Return Statement
```cpp
return 0;
```
- Indicates that the program ended successfully.

## Example Output
If the user enters the number `234`, the output will be:
```
Enter a number: 234
Sum of its digits is: 9
Product of its digits is: 24
After subtraction (Product - Sum): 15
```

## Compilation and Execution
1. **Compile the program** using a C++ compiler:
   ```bash
   g++ -o subtract_product_sum subtract_product_sum.cpp
   ```
2. **Run the compiled program**:
   ```bash
   ./subtract_product_sum
   ```
3. **Follow the prompt** to enter an integer.

## Notes
- The program currently does not handle negative integers or non-integer inputs. You can extend it by adding input validation.
- This program demonstrates basic control structures in C++, which can be useful for beginners learning the language.
