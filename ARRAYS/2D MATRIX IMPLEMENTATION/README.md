# 2D Matrix Implementation in C++

This project implements a simple C++ program to create and display a 2D matrix based on user input.

## Features

- Accepts the number of rows and columns from the user.
- Allows the user to input matrix elements.
- Displays the matrix in a formatted way.

## Requirements

- A C++ compiler (e.g., g++, clang++).
- Standard C++ library.

## Usage

1. Clone the repository or download the source code.
2. Open your terminal and navigate to the project directory.
3. Compile the code using a C++ compiler. For example:
   ```bash
   g++ -o matrix matrix.cpp
   ```
4. Run the compiled program:
   ```bash
   ./matrix
   ```
5. Follow the prompts to enter the number of rows, columns, and the matrix elements.

## Example

### Input/Output Example

```
Enter the number of rows: 2
Enter the number of columns: 3
Enter the elements of the matrix:
1 2 3
4 5 6

Output:
1 2 3 
4 5 6 
```

### Explanation

1. **Input Phase**:
   - The program first prompts the user to enter the number of rows and columns for the matrix. In this case, the user entered `2` rows and `3` columns.
   - Next, the user is prompted to input the elements of the matrix. The user inputs the elements row by row:
     - First row: `1 2 3`
     - Second row: `4 5 6`

2. **Output Phase**:
   - After the input is complete, the program displays the matrix in a formatted manner. Each row of the matrix is printed on a new line for clarity.

## Code Explanation

- **`print` Function**: This function takes a constant reference to a 2D vector and its dimensions as arguments and prints the matrix to the console. It iterates through each element and outputs them with spaces in between.
  
- **`main` Function**: 
  - It starts by gathering the number of rows and columns from the user.
  - It then initializes a 2D vector with the specified dimensions.
  - After that, it prompts the user to fill the matrix elements.
  - Finally, it calls the `print` function to display the matrix.

## Complexity Analysis

- **Time Complexity**:
  - The time complexity for this implementation is \(O(n \times m)\), where \(n\) is the number of rows and \(m\) is the number of columns. This is because we need to fill each element of the matrix and then print each element.

- **Space Complexity**:
  - The space complexity is also \(O(n \times m)\), as we are using a 2D vector to store the matrix elements.
