# Linear Search Program

This C++ program implements a linear search algorithm to find an element in an array. It allows users to input the size of the array, its elements, and the key they want to search for.

## Features

- Takes input for the size of the array and validates it.
- Accepts integer elements for the array.
- Searches for a specified key using linear search.
- Outputs whether the key is found in the array.

## Getting Started

### Prerequisites

- A C++ compiler (e.g., g++, clang++).
- Basic knowledge of C++ syntax and command line usage.

### Compilation

To compile the program, use the following command:

```bash
g++ -o linear_search linear_search.cpp
```

Replace `linear_search.cpp` with the name of your source file.

### Running the Program

After compilation, run the program with the following command:

```bash
./linear_search
```

### Input

1. The program will prompt you to enter the size of the array. The size must be between 1 and 100.
2. Enter the elements of the array one by one, separated by spaces or new lines.
3. Finally, enter the element you wish to search for in the array.

## Example

### Input

```
Enter the size of the array: 5
Enter the elements of the array: 10 20 30 40 50
Enter the element you want to search: 30
```

### Step-by-Step Explanation

1. **Enter Size of the Array**: 
   - The program prompts: `Enter the size of the array:`
   - The user inputs `5`, indicating that they will enter five elements for the array.

2. **Enter Array Elements**: 
   - The program then prompts: `Enter the elements of the array:`
   - The user enters `10`, `20`, `30`, `40`, and `50`. These values are stored in the array in the order they are entered:
     - `arr[0] = 10`
     - `arr[1] = 20`
     - `arr[2] = 30`
     - `arr[3] = 40`
     - `arr[4] = 50`

3. **Enter Key Element**:
   - The program prompts: `Enter the element you want to search:`
   - The user inputs `30`, which is the value they want to find in the array.

4. **Searching for the Key**:
   - The program calls the `linearSearch` function, which checks each element of the array sequentially:
     - First, it checks `arr[0]` (10) against the key (30) → Not a match.
     - Next, it checks `arr[1]` (20) → Not a match.
     - Then, it checks `arr[2]` (30) → **Match found!**

5. **Output Result**:
   - Since the key `30` is found in the array, the program outputs:
     ```
     Element is found.
     ```

### Output

```
Element is found.
```

## Important Information

- **Input Validation**: The program checks if the entered size is between 1 and 100. If the input is invalid, it prompts the user with an error message and terminates.
- **Time Complexity**: The linear search algorithm has a time complexity of O(n), where n is the number of elements in the array. This means that in the worst-case scenario, the program may need to check every element.
- **Space Complexity**: The space complexity is O(1) because the algorithm uses a constant amount of space regardless of the input size.

## Code Structure

- **linearSearch**: Function that implements the linear search algorithm.
- **main**: Entry point of the program where user input is handled and the search function is called.
