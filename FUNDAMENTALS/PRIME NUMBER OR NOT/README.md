# Prime Number Checker

This is a simple C++ program that checks whether a given number is prime or not.

## Overview

A prime number is a natural number greater than 1 that cannot be formed by multiplying two smaller natural numbers. In other words, a prime number has exactly two distinct positive divisors: 1 and itself. For example, the numbers 2, 3, 5, and 7 are prime numbers, while 4, 6, 8, and 9 are not.

This program prompts the user to enter a number, and then determines whether that number is prime by checking for divisibility.

## Code Explanation

Here is the code for the prime number checker:

```cpp
#include <iostream>
using namespace std;

int main() {
    int number;
    cout << "Enter a number to check if it is prime: " << endl;
    cin >> number;

    bool isPrime = true;

    for (int i = 2; i < number; i++) {
        if (number % i == 0) {
            isPrime = false;
            break;
        }
    }

    if (isPrime) {
        cout << "It is a prime number." << endl;
    } else {
        cout << "It is not a prime number." << endl;
    }

    return 0;
}
```

### Breakdown of the Code

1. **Header Inclusion**:
   ```cpp
   #include <iostream>
   ```
   This line includes the iostream library, which is necessary for input and output operations in C++.

2. **Using Namespace**:
   ```cpp
   using namespace std;
   ```
   This allows us to use names from the standard library without prefixing them with `std::`.

3. **Main Function**:
   ```cpp
   int main() {
   ```
   The program execution starts from the `main` function.

4. **Variable Declaration**:
   ```cpp
   int number;
   ```
   Here, we declare an integer variable named `number` to store the user input.

5. **User Input**:
   ```cpp
   cout << "Enter a number to check if it is prime: " << endl;
   cin >> number;
   ```
   This prompts the user to enter a number, which is then stored in the `number` variable.

6. **Prime Check Initialization**:
   ```cpp
   bool isPrime = true;
   ```
   We initialize a boolean variable `isPrime` to `true`. This variable will help us determine if the number is prime.

7. **Loop for Divisibility Check**:
   ```cpp
   for (int i = 2; i < number; i++) {
       if (number % i == 0) {
           isPrime = false;
           break;
       }
   }
   ```
   This loop runs from 2 to `number - 1`. For each `i`, it checks if `number` is divisible by `i`. If it finds any divisor, it sets `isPrime` to `false` and exits the loop.

8. **Result Output**:
   ```cpp
   if (isPrime) {
       cout << "It is a prime number." << endl;
   } else {
       cout << "It is not a prime number." << endl;
   }
   ```
   After the loop, it checks the value of `isPrime`. If it's still `true`, it prints that the number is prime; otherwise, it states that it is not prime.

9. **Return Statement**:
   ```cpp
   return 0;
   ```
   This indicates that the program ended successfully.

## How to Compile and Run

1. **Save the Code**: Copy the code into a file named `prime_checker.cpp`.

2. **Open a Terminal**: Navigate to the directory where `prime_checker.cpp` is located.

3. **Compile the Program**:
   ```bash
   g++ -o prime_checker prime_checker.cpp
   ```
   This command compiles the code and generates an executable named `prime_checker`.

4. **Run the Program**:
   ```bash
   ./prime_checker
   ```
   Execute the compiled program.

5. **Input**: When prompted, enter a positive integer to check if it is prime.

## Example Usage

```
Enter a number to check if it is prime: 
7
It is a prime number.
```

```
Enter a number to check if it is prime: 
10
It is not a prime number.
```

## Limitations

- The program currently only checks for positive integers greater than 1. It does not handle negative numbers or zero.
- The performance may degrade for large numbers since it checks all integers up to `number - 1`.

## Future Improvements

1. **Optimization**:
   - Modify the loop to check only up to the square root of the number for efficiency.
   - Implement a more efficient algorithm, such as the Sieve of Eratosthenes, for generating prime numbers.

2. **Input Validation**:
   - Add checks to ensure the user inputs a valid positive integer.
   - Handle cases where the input is not an integer (e.g., strings or special characters).

3. **Range Check**:
   - Allow users to check all prime numbers within a specified range.
