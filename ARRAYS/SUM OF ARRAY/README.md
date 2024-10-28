# Sum of Array

This C++ program calculates the sum of an array of integers entered by the user. It includes functions for traversing and printing the array elements.

## Features

- Prompts the user to enter the size of the array (up to 100 elements).
- Validates the input size to ensure it is within a valid range.
- Accepts integer inputs to populate the array.
- Displays the elements of the array.
- Computes and outputs the sum of the array elements.

## Example

### Input
```
Enter the size of the array: 5
Enter the elements of the array: 
10
20
30
40
50
```

### Output
```
Elements of the array: 10 20 30 40 50 
Sum of array is: 150
```

### Explanation

1. **User Input:**
   - The user is prompted to enter the size of the array. In this case, the user inputs `5`.
   - Next, the user is prompted to enter the elements of the array. The user enters `10`, `20`, `30`, `40`, and `50`.

2. **Array Traversing:**
   - The program displays the elements of the array as `10 20 30 40 50`.

3. **Sum Calculation:**
   - The program computes the sum of the elements: 
     - `10 + 20 + 30 + 40 + 50 = 150`.
   - Finally, it outputs the sum: `Sum of array is: 150`.

## Important Information

- **Input Validation:** The program checks if the input size is between 1 and 100. If the size is invalid, it informs the user and exits the program.
- **Array Limitations:** The program uses a static array with a maximum size of 100 elements. For larger datasets, consider using dynamic memory allocation or data structures like `std::vector`.

## Time and Space Complexity

- **Time Complexity:** 
  - The time complexity of both the traversing and summing functions is O(n), where n is the size of the array. Each element is processed once.
  
- **Space Complexity:** 
  - The space complexity is O(1) for the sum calculation since it uses a fixed amount of additional space (the variable for sum). The array itself takes O(n) space.

## Requirements

- A C++ compiler (e.g., g++, Visual Studio, etc.)
- Basic knowledge of C++ programming

## How to Run the Program

1. **Clone or Download the Repository:**
   - Clone the repository using:
     ```bash
     git clone <repository-url>
     ```
   - Or download it as a ZIP file and extract it.

2. **Compile the Program:**
   Navigate to the directory containing the source file and compile it using:
   ```bash
   g++ -o sum_of_array sum_of_array.cpp
   ```

3. **Run the Program:**
   Execute the compiled program:
   ```bash
   ./sum_of_array
   ```

4. **Follow the Prompts:**
   - Enter the desired size of the array (between 1 and 100).
   - Input the elements of the array when prompted.
