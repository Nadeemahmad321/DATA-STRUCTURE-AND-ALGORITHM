# Triplet Sum Finder

## Description
The Triplet Sum Finder is a C++ program that identifies and prints all unique triplets in a given array that sum up to a specified target value. This program is useful for problems involving combinations of numbers and can serve as a foundation for more complex algorithms.

## Features
- Accepts user input for the size of the array and its elements.
- Prompts the user for a target sum.
- Efficiently finds and displays all triplets that sum to the specified target.

## How It Works
1. **Input**: The user is prompted to enter the size of the array and the elements.
2. **Triplet Search**: The program utilizes three nested loops to examine all possible combinations of three different elements in the array.
3. **Output**: Each triplet that meets the criteria is printed on a new line.

## Complexity Analysis
- **Time Complexity**: \(O(n^3)\)
  - The program uses three nested loops to explore combinations of elements. This results in a cubic time complexity, making it less efficient for larger arrays.
- **Space Complexity**: \(O(1)\)
  - The program uses a constant amount of extra space, regardless of the input size, as it only stores a few variables.

## Example

### Input:
```
Enter the size of array: 6
Enter the elements of array: 1 2 3 4 5 6
Enter the key: 10
```

### Explanation:
1. **Array Elements**: The user inputs the elements `[1, 2, 3, 4, 5, 6]`.
2. **Target Sum**: The user specifies the target sum as `10`.
3. **Triplet Evaluation**:
   - The program will evaluate all possible combinations of three different elements:
     - `(1, 2, 3)` → Sum = 6 (not a match)
     - `(1, 2, 4)` → Sum = 7 (not a match)
     - `(1, 2, 5)` → Sum = 8 (not a match)
     - `(1, 2, 6)` → Sum = 9 (not a match)
     - `(1, 3, 4)` → Sum = 8 (not a match)
     - `(1, 3, 5)` → Sum = 9 (not a match)
     - `(1, 3, 6)` → Sum = 10 (match found)
     - `(1, 4, 5)` → Sum = 10 (match found)
     - `(1, 4, 6)` → Sum = 11 (not a match)
     - `(2, 3, 4)` → Sum = 9 (not a match)
     - `(2, 3, 5)` → Sum = 10 (match found)
     - And so on...
4. **Output**:
   ```
   Triplet sums are:
   (1, 3, 6)
   (1, 4, 5)
   (2, 3, 5)
   ```

## Usage
1. Compile the program using a C++ compiler:
   ```bash
   g++ triplet_sum.cpp -o triplet_sum
   ```

2. Run the executable:
   ```bash
   ./triplet_sum
   ```

3. Follow the prompts to enter the size of the array, the array elements, and the target sum.

## Important Information
- The maximum size of the array is set to 100 elements.
- The program does not check for duplicate triplets; it may output the same triplet if they are formed from different indexes.
- This implementation is suitable for educational purposes and smaller input sizes. For larger inputs, consider using optimized algorithms.


### Key Additions:
- **Full Explanation of Example**: The example section now provides a detailed breakdown of the input, how the program evaluates combinations, and what the output means.
- **Complexity Analysis**: Included sections on time and space complexity to give users insight into the program's performance.
- **Important Information**: Added details about limitations and use cases.
