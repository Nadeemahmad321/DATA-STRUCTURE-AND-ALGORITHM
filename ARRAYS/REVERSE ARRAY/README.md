# Array Traversal and Reversal

This C++ program demonstrates how to traverse and reverse an array of integers. It allows users to input the size of the array and its elements, then outputs the array before and after reversing.

## Features

- Prompts the user for the size of the array (up to 100 elements).
- Allows the user to input the array elements.
- Displays the elements of the array before and after reversing.

## Code Explanation

### Functions

1. **`traversingArray(int arr[], int size)`**:
   - **Purpose**: Traverses through the given array and prints its elements.
   - **Parameters**: 
     - `arr[]`: An array of integers.
     - `size`: The number of elements in the array.
   - **How it Works**: A for loop iterates through the array, printing each element followed by a space. A newline is printed at the end for better formatting.

2. **`reverseArray(int arr[], int size)`**:
   - **Purpose**: Reverses the elements of the array in place.
   - **Parameters**: 
     - `arr[]`: An array of integers.
     - `size`: The number of elements in the array.
   - **How it Works**: 
     - Two pointers are initialized: one at the start (`start`) and one at the end (`end`) of the array.
     - The elements at these positions are swapped, and the pointers are moved toward each other until they meet.

### Main Function

- Prompts the user to enter the size of the array and validates the input.
- Reads the elements of the array from user input.
- Calls `traversingArray` to display the original array.
- Calls `reverseArray` to reverse the array.
- Displays the reversed array using `traversingArray`.

## Example

```plaintext
Enter the size of the array: 5
Enter the elements of the array:
1
2
3
4
5
Elements of the array before reverse: 1 2 3 4 5 
Elements of the array after reverse: 5 4 3 2 1 
```

### Explanation of Example

1. **User Input**:
   - The user is prompted to enter the size of the array. In this example, they enter `5`.
   - The user then enters the elements of the array: `1`, `2`, `3`, `4`, and `5`.

2. **Output Before Reversal**:
   - The program displays: `Elements of the array before reverse: 1 2 3 4 5`.

3. **Reversal Process**:
   - The `reverseArray` function is called. It swaps:
     - `arr[0]` (1) with `arr[4]` (5)
     - `arr[1]` (2) with `arr[3]` (4)
   - The middle element (3) remains in place since the array length is odd.

4. **Output After Reversal**:
   - The program displays: `Elements of the array after reverse: 5 4 3 2 1`.

## Complexity Analysis

- **Time Complexity**:
  - Traversing the array takes \(O(n)\) time, where \(n\) is the number of elements in the array.
  - Reversing the array also takes \(O(n)\) time due to the single pass through the array using two pointers.
  - Overall, the time complexity is \(O(n)\).

- **Space Complexity**:
  - The space complexity is \(O(1)\) since the reversal is done in place and no additional arrays or significant memory is used.

## Important Information

- Ensure that the user inputs a valid size for the array (between 1 and 100). If the input is invalid, the program will exit with an error message.
- This program is designed for educational purposes and can be modified or expanded to include more features, such as dynamic memory allocation or error handling for non-integer inputs.

## Compilation and Execution

To compile and run the program, use the following commands:

```bash
g++ -o array_traversal array_traversal.cpp
./array_traversal

