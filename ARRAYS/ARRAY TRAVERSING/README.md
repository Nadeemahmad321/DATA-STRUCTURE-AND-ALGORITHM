# Array Traversal in C++

This program allows users to create an array, input its size and elements, and then traverse the array to display its contents.

## Features

- Prompts the user to enter the size of the array (up to 100 elements).
- Validates the size input to ensure it falls within a valid range.
- Allows users to input elements of the array.
- Traverses the array and prints each element.

## Requirements

- A C++ compiler (e.g., g++, clang++).
- Standard C++ library.

## Usage

1. **Compile the Program:**
   To compile the code, use the following command in your terminal:
   ```bash
   g++ -o array_traversal array_traversal.cpp
   ```

2. **Run the Program:**
   Execute the compiled program with:
   ```bash
   ./array_traversal
   ```

3. **Input Instructions:**
   - When prompted, enter the size of the array (must be between 1 and 100).
   - Then, input the elements of the array, separated by spaces.

## Example

### Sample Input and Output
```
Enter the size of the array: 5
Enter the elements of the array:
10 20 30 40 50
Elements of the array are: 10 20 30 40 50
```

### Explanation

1. **User Input:**
   - The program first prompts the user to enter the size of the array. In this case, the user inputs `5`, which is valid.
   
2. **Element Input:**
   - The user is then prompted to enter `5` integers, which are `10`, `20`, `30`, `40`, and `50`.

3. **Output:**
   - After storing these elements in the array, the program traverses the array using the `traversingArray` function, which prints each element in order.

### Important Information

- **Input Validation:** The program checks if the entered size is valid (between 1 and 100). If the input is invalid, it displays an error message and exits.
- **Array Size Limitation:** The array is statically allocated with a maximum size of 100. Adjustments can be made for larger sizes if necessary, but dynamic memory allocation would be required.

## Complexity Analysis

- **Time Complexity:**
  - The time complexity for traversing the array is \(O(n)\), where \(n\) is the size of the array. This is because the program iterates through the array once to print its elements.

- **Space Complexity:**
  - The space complexity is \(O(1)\) for the traversal function since it uses a constant amount of space for variables, independent of the input size.
  - The space used for the array itself is \(O(n)\) due to the storage of \(n\) integers.
