# Duplicate Finder in an Array

This program identifies a duplicate element in an array using the XOR operation. It assumes there is exactly one duplicate in an array of integers ranging from 0 to `size - 2`, where the size of the array is `size`.

## How It Works

### Key Concepts

- **XOR Operation**: 
  - The XOR operation has properties that are useful for this problem:
    - \( a \oplus a = 0 \)
    - \( a \oplus 0 = a \)
  - By XORing all elements of the array and all numbers from 0 to `size - 2`, the result will be the duplicate element because all other numbers will cancel out.

### Complexity

- **Time Complexity**: \( O(n) \) 
  - The algorithm iterates through the array and the range of numbers, making it linear in terms of the size of the input.

- **Space Complexity**: \( O(1) \)
  - Only a constant amount of extra space is used (for variables).

## Example with Step-by-Step Explanation

### Input Example

Let's say the user inputs the following:

```
Enter the size of the array (should be >= 2): 5
Enter the elements of the array (values should be from 0 to 3): 0 1 2 3 1
```

### Step-by-Step Execution

1. **Initialization**:
   - `ans` is initialized to `0`.

2. **XOR all elements of the array**:
   - Iterate through the array `[0, 1, 2, 3, 1]`:
     - `ans = 0 ^ 0 = 0`
     - `ans = 0 ^ 1 = 1`
     - `ans = 1 ^ 2 = 3`
     - `ans = 3 ^ 3 = 0`
     - `ans = 0 ^ 1 = 1`
   - After this loop, `ans` is `1`.

3. **XOR with numbers from 0 to size - 2 (0 to 3)**:
   - Iterate through the range `0` to `3`:
     - `ans = 1 ^ 0 = 1`
     - `ans = 1 ^ 1 = 0`
     - `ans = 0 ^ 2 = 2`
     - `ans = 2 ^ 3 = 1`
   - After this loop, `ans` is again `1`.

4. **Result**:
   - The function returns `1`, which is the duplicate element in the array.

### Output Example

```
Duplicate element in the array is: 1
```

## Code Structure

- **Function**: `findDuplicate(int arr[], int size)`
  - Takes an array and its size as parameters.
  - Returns the duplicate element.

- **Main Function**:
  - Handles user input and output.
  - Validates the size of the array.

## Important Information

- Ensure the input values are within the specified range (0 to `size - 2`).
- The program is designed for educational purposes to demonstrate the XOR technique for finding duplicates efficiently in linear time and constant space.

## Compilation and Execution

### Requirements

- C++ compiler (C++11 or later recommended)

### Steps to Compile and Run

1. Save the code in a file named `duplicate_finder.cpp`.
2. Open your terminal/command prompt.
3. Navigate to the directory where `duplicate_finder.cpp` is located.
4. Compile the program:
   ```bash
   g++ -o duplicate_finder duplicate_finder.cpp
   ```
5. Run the executable:
   ```bash
   ./duplicate_finder
   ```
