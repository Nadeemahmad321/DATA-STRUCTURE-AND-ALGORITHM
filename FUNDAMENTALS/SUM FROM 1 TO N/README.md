# Sum from 1 to N

This program calculates the sum of all integers from 1 to a user-defined number \( n \). It demonstrates two different approaches: using a `for` loop and a `while` loop.

## Features

- Prompts the user to input a number.
- Computes the sum using both a `for` loop and a `while` loop.
- Displays the results of both calculations.

## How to Use

1. Compile the program using a C++ compiler.
2. Run the executable.
3. Enter a positive integer when prompted.
4. View the sum of numbers from 1 to \( n \) calculated by both methods.

## Example Output

```
Enter the number you want to sum: 5
Sum of numbers from 1 to 5 is: 15

Sum of numbers from 1 to 5 is: 15
```

## Code Explanation

### Full Code

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    cout << "Enter the number you want to sum: ";
    cin >> n;

    // Using for loop to calculate the sum from 1 to n
    int sum = 0;
    for (int i = 1; i <= n; i++) {
        sum += i;
    }
    cout << "Sum of numbers from 1 to " << n << " is: " << sum << endl << endl;

    // Using while loop to calculate the sum from 1 to n
    sum = 0;
    int i = 1;
    while (i <= n) {
        sum += i;
        i++;
    }
    cout << "Sum of numbers from 1 to " << n << " is: " << sum << endl;

    return 0;
}
```

### Detailed Explanation of Loops

#### 1. **For Loop**

```cpp
int sum = 0;
for (int i = 1; i <= n; i++) {
    sum += i;
}
```

- **Initialization**: The loop starts by initializing `i` to 1.
- **Condition**: The loop continues as long as `i` is less than or equal to `n`.
- **Iteration**: After each iteration, `i` is incremented by 1.
- **Body**: Inside the loop, the current value of `i` is added to `sum` using the `+=` operator. This means `sum` accumulates the values of `i` from 1 to \( n \).

This loop structure is ideal for situations where the number of iterations is known beforehand (in this case, the value of \( n \)).

#### 2. **While Loop**

```cpp
sum = 0;
int i = 1;
while (i <= n) {
    sum += i;
    i++;
}
```

- **Initialization**: Before the loop starts, `sum` is reset to 0, and `i` is initialized to 1.
- **Condition**: The loop runs as long as `i` is less than or equal to \( n \).
- **Body**: Similar to the `for` loop, the current value of `i` is added to `sum`.
- **Iteration**: After the addition, `i` is incremented by 1.

The `while` loop is more flexible for scenarios where the number of iterations is not known in advance. However, in this case, both loops effectively achieve the same result.

### Output

After executing both loops, the program prints the total sum calculated by each method, confirming that both approaches yield the same result.

## Requirements

- A C++ compiler (e.g., g++, clang++).
- Basic understanding of C++ syntax and concepts like loops and user input.
