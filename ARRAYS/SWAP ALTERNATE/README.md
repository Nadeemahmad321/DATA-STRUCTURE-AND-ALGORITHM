# Alternate Swap Array Elements

## Overview
This C++ program takes an array of integers as input and swaps its elements in pairs. If the array has an odd number of elements, the last element remains unchanged.

## Features
- Input the size of the array.
- Input the elements of the array.
- Swap elements in pairs.
- Print the modified array.

## How It Works
1. The program prompts the user to enter the size of the array.
2. It then asks the user to input the elements of the array.
3. The `alternateSwap` function swaps adjacent elements.
4. Finally, the modified array is printed.

## Example
### Input/Output Example
```plaintext
Enter the size of array: 6
Enter the elements of the array: 10 20 30 40 50 60
Output: 20 10 40 30 60 50
```

### Explanation
- **Input**: The user enters `6` as the size of the array and `10, 20, 30, 40, 50, 60` as the elements.
- **Swapping Process**:
  - The first pair (`10` and `20`) is swapped to become `20 10`.
  - The second pair (`30` and `40`) is swapped to become `40 30`.
  - The third pair (`50` and `60`) is swapped to become `60 50`.
- **Output**: The final modified array is `20 10 40 30 60`.

## Time and Space Complexity
- **Time Complexity**: O(n)
  - The function iterates through the array once, performing a constant-time operation (swap) for each pair.
  
- **Space Complexity**: O(1)
  - The algorithm uses a constant amount of extra space, regardless of the input size, as it swaps elements in place.

## Requirements
- C++11 or later
- A C++ compiler (e.g., g++, clang++)

## Usage
1. Compile the program using a C++ compiler:
   ```bash
   g++ -o alternate_swap alternate_swap.cpp
   ```
2. Run the executable:
   ```bash
   ./alternate_swap
   ```
3. Follow the prompts to enter the size and elements of the array.

## Important Information
- The program assumes that the user will enter a valid size and corresponding elements.
- The maximum size of the array is set to 100, but this can be modified as needed.

### Key Additions:
- **Example Section**: A complete input/output example with detailed explanations.
- **Complexity Analysis**: Included both time and space complexity analyses for better understanding of performance.
- **Important Information**: Added a note about user input assumptions and maximum array size.
