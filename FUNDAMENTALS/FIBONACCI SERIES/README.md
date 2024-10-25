# Fibonacci Series Generator

This C++ program generates the Fibonacci series up to a user-specified term. The Fibonacci series starts with 0 and 1, with each subsequent term being the sum of the two preceding terms.

## Features

- Prompts the user for the desired term in the Fibonacci series.
- Outputs the series up to that term.
- Handles the first two terms separately for clarity.

## How to Use

1. **Set Up**: Make sure you have a C++ compiler installed (like g++ or any IDE that supports C++ development).
2. **Copy the Code**: Copy the code into a `.cpp` file (e.g., `fibonacci.cpp`).
3. **Compile the Program**: Use the command below to compile the program:
   ```bash
   g++ fibonacci.cpp -o fibonacci
   ```
4. **Run the Program**: Execute the compiled program:
   ```bash
   ./fibonacci
   ```
5. **Input**: Enter the term number you want to see in the Fibonacci series when prompted.

## Code Explanation

Here’s a detailed breakdown of the code:

```cpp
#include <iostream>
using namespace std;

int main() {
    int firstTerm = 0;     // The first term of the Fibonacci series
    int secondTerm = 1;    // The second term of the Fibonacci series
    int thirdTerm;         // To hold the next term in the series

    int nthTerm;           // Variable to store user input for the term to generate
    cout << "Enter the term you want: ";
    cin >> nthTerm;       // Get user input for the term number

    // Check for the first term
    if (nthTerm == 1) {
        cout << "Fibonacci series: " << firstTerm << endl;
    } 
    // Check for the second term
    else if (nthTerm == 2) {
        cout << "Fibonacci series: " << firstTerm << ", " << secondTerm << endl;
    } 
    // Calculate for terms greater than 2
    else {
        cout << "Fibonacci series: " << firstTerm << ", " << secondTerm;
        for (int i = 3; i <= nthTerm; i++) {
            thirdTerm = firstTerm + secondTerm; // Calculate the next term
            cout << ", " << thirdTerm; // Output the next term
            firstTerm = secondTerm;    // Update firstTerm to secondTerm
            secondTerm = thirdTerm;     // Update secondTerm to thirdTerm
        }
        cout << endl; // New line after the series
    }

    return 0; // End of program
}
```

### Detailed Explanation of Key Components

1. **Header Files**:
   - `#include <iostream>`: This includes the input-output stream library, allowing us to use `cin` and `cout` for user input and output.

2. **Variables**:
   - `firstTerm` and `secondTerm`: Initialized to 0 and 1, these represent the first two terms of the Fibonacci series.
   - `thirdTerm`: Used to calculate the next term in the series.
   - `nthTerm`: Stores the user’s input for how many terms of the Fibonacci series to generate.

3. **User Input**:
   - The program prompts the user to enter the term they wish to see, which is stored in `nthTerm`.

4. **Conditional Logic**:
   - The program checks the value of `nthTerm`:
     - If it is 1, it prints just the first term (0).
     - If it is 2, it prints the first two terms (0, 1).
     - If it is greater than 2, it enters a loop to calculate the Fibonacci series up to `nthTerm`.

5. **Loop for Series Calculation**:
   - The `for` loop starts from 3 (since the first two terms are already handled) and continues until it reaches `nthTerm`.
   - Inside the loop:
     - `thirdTerm` is calculated as the sum of `firstTerm` and `secondTerm`.
     - The new term is printed.
     - `firstTerm` and `secondTerm` are updated for the next iteration.

6. **Output**:
   - The series is displayed in a comma-separated format, making it easy to read.

## Example Output

Here's how the program runs with an example input:

```
Enter the term you want: 5
Fibonacci series: 0, 1, 1, 2, 3
```

## Notes

- **Input Validation**: The program does not currently handle invalid inputs (like negative numbers or non-integer values). Implementing input validation is recommended for production use.
- **Extensibility**: This code can be expanded to calculate larger Fibonacci numbers or to display the entire series up to a specified limit.

This simple program effectively demonstrates the basic principles of loops, conditionals, and user interaction in C++. Happy coding!
