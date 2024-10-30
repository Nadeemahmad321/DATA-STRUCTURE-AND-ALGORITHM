# 3D Matrix Implementation

This C++ program allows users to create and manipulate a 3D matrix. Users can input the dimensions of the matrix and its elements, and the program will then display the matrix in a structured format.

## Features

- Dynamic creation of a 3D matrix based on user-defined dimensions.
- Input of matrix elements from the user.
- Printing the entire 3D matrix with clear page separation.

## Requirements

- C++11 or higher
- A standard C++ compiler (e.g., g++, clang++)

## Usage

1. **Compile the program** using a C++ compiler:
   ```bash
   g++ -o 3d_matrix 3d_matrix.cpp
   ```

2. **Run the program**:
   ```bash
   ./3d_matrix
   ```

3. **Follow the prompts** to enter:
   - The number of rows
   - The number of columns
   - The number of pages
   - The elements of the matrix

4. The program will display the 3D matrix organized by pages.

## Example with Step-by-Step Solution

### Step 1: Compile and Run the Program

After compiling the program, run it:

```bash
./3d_matrix
```

### Step 2: Input Dimensions

You will be prompted to enter the dimensions of the matrix. For this example, we'll use:
- Rows: `2`
- Columns: `2`
- Pages: `2`

**Input:**
```
Enter the number of rows: 2
Enter the number of columns: 2
Enter the number of pages: 2
```

### Step 3: Input Matrix Elements

Next, you will enter the elements for the 3D matrix. For this example, we will fill the matrix as follows:
- Page 0: 
  - Row 0: `1`, `2`
  - Row 1: `3`, `4`
  
- Page 1:
  - Row 0: `5`, `6`
  - Row 1: `7`, `8`

**Input:**
```
Enter the elements of the matrix:
1 2
3 4
5 6
7 8
```

### Step 4: Output the Matrix

The program will then print the 3D matrix in a structured format. The output will show each page with its respective rows and columns.

**Output:**
```
3D matrix implementation:
Page 0:
1 2 
3 4 

Page 1:
5 6 
7 8 
```

### Final Structure of the Matrix

The resulting 3D matrix can be visualized as follows:

```
Page 0:
Row 0: [1, 2]
Row 1: [3, 4]

Page 1:
Row 0: [5, 6]
Row 1: [7, 8]
```

## Important Information

- **Dynamic Memory Allocation**: The program uses `std::vector` for dynamic memory allocation, allowing it to handle varying matrix sizes without needing to know dimensions at compile time.
- **Input Validation**: The current implementation does not include input validation. Users should ensure they enter valid integers for dimensions and matrix elements.
- **Complexity**: 
  - **Time Complexity**: The time complexity for creating and populating the matrix is \(O(n \cdot m \cdot p)\), where \(n\) is the number of rows, \(m\) is the number of columns, and \(p\) is the number of pages. Printing the matrix also takes \(O(n \cdot m \cdot p)\).
  - **Space Complexity**: The space complexity is \(O(n \cdot m \cdot p)\) due to the storage of the matrix in memory.

## Code Structure

- **`print` Function**: Responsible for printing the 3D matrix.
- **`main` Function**: Handles user input, matrix creation, and calls the print function.
