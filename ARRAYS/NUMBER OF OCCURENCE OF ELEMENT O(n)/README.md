# Count Occurrences of an Element in an Array

This C++ program counts the number of occurrences of a specified element (key) in an array provided by the user.

## Features

- User-defined array size and elements.
- User can specify the key element to search for.
- Displays the number of times the key appears in the array.

## How It Works

1. The program prompts the user to enter the size of the array.
2. The user inputs the elements of the array.
3. The user specifies the key element they wish to count.
4. The program calculates and displays the number of occurrences of the key element in the array.

## Code Structure

- **numberOfOccurence**: A function that takes a vector of integers and a key integer, returning the count of how many times the key appears in the vector.
- **main**: The entry point of the program that handles user input and output.

## Example

### Input
```plaintext
Enter the size of arr: 5
Enter the element of array: 1 2 3 2 1
Enter the key element: 2
```

### Output
```plaintext
Number of occurrence of element: 2
```

### Explanation
1. **Input Size**: The user enters `5`, which means the array will have 5 elements.
2. **Array Elements**: The user inputs `1`, `2`, `3`, `2`, `1`. This forms the array: `[1, 2, 3, 2, 1]`.
3. **Key Element**: The user specifies `2` as the key.
4. **Counting Occurrences**: The program iterates through the array and counts how many times `2` appears:
   - It finds `2` at index `1` (first occurrence).
   - It finds `2` again at index `3` (second occurrence).
5. The output shows that the number `2` appears `2` times in the array.

## Complexity Analysis

- **Time Complexity**: O(n), where n is the number of elements in the array. The program needs to iterate through the entire array to count occurrences.
- **Space Complexity**: O(1), since we are using a fixed amount of space for the count variable, regardless of the input size.

## Usage

1. Compile the code using a C++ compiler (e.g., g++):

   ```bash
   g++ -o count_occurrences count_occurrences.cpp
   ```

2. Run the compiled program:

   ```bash
   ./count_occurrences
   ```

3. Follow the prompts to enter the size of the array, the array elements, and the key element.

## Important Information

- Ensure that you enter the correct data types (integers) for the array and key element.
- The program does not handle invalid inputs (like negative sizes or non-integer values). You may consider adding input validation for robustness.
