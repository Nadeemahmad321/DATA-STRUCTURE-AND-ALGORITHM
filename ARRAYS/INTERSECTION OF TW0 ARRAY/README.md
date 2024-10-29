# Intersection of Two Sorted Arrays

This program finds the intersection of two arrays (vectors) of integers. The intersection is defined as the set of elements that are present in both arrays.

## Features

- Accepts two vectors of integers from the user.
- Sorts the input vectors if they are not sorted.
- Calculates the intersection while avoiding duplicates in the result.

## Requirements

- C++11 or later
- Standard Template Library (STL)

## How to Use

1. **Compile the Program**:
   Use a C++ compiler to compile the program. For example, with g++, run:
   ```bash
   g++ -o intersection intersection.cpp
   ```

2. **Run the Program**:
   Execute the compiled program:
   ```bash
   ./intersection
   ```

3. **Input**:
   - The program will prompt you to enter the size of the first vector.
   - It will then ask you to input the elements of the first vector.
   - Next, it will ask for the size of the second vector and the elements of that vector.

4. **Output**:
   The program will display the intersection of the two vectors.

## Example with Step-by-Step Solution

### Input
```
Enter the size of a vector: 5
Enter elements of vector a: 1 2 2 3 4
Enter the size of b vector: 4
Enter elements of vector b: 2 2 3 5
```

### Step-by-Step Solution

1. **Sort the Vectors**:
   - Vector A: `[1, 2, 2, 3, 4]`
   - Vector B: `[2, 2, 3, 5]`

2. **Initialize Pointers**:
   - `i = 0` (for vector A)
   - `j = 0` (for vector B)
   - `ans = []` (to store the intersection)

3. **Iterate Through Both Vectors**:
   - Compare `a[i]` and `b[j]`:
     - **Iteration 1**: `a[0] = 1`, `b[0] = 2` → `1 < 2` → Increment `i` to `1`
     - **Iteration 2**: `a[1] = 2`, `b[0] = 2` → `2 == 2` → Add `2` to `ans` → Increment `i` to `2`, `j` to `1`
     - **Iteration 3**: `a[2] = 2`, `b[1] = 2` → `2 == 2` → Skip adding (to avoid duplicates) → Increment `i` to `3`, `j` to `2`
     - **Iteration 4**: `a[3] = 3`, `b[2] = 3` → `3 == 3` → Add `3` to `ans` → Increment `i` to `4`, `j` to `3`
     - **Iteration 5**: `a[4] = 4`, `b[3] = 5` → `4 < 5` → Increment `i` to `5`

4. **End of Iteration**:
   - `i` exceeds the size of vector A, stop the iteration.

### Final Output
```
Intersection of the two arrays is: 2 3 
```

## Time Complexity

- **Sorting**: \(O(n \log n + m \log m)\) where \(n\) is the size of vector A and \(m\) is the size of vector B.
- **Intersection Finding**: \(O(n + m)\) in the worst case, where you traverse both vectors.
- **Overall Complexity**: \(O(n \log n + m \log m)\) due to the sorting step being the dominant factor.

## Important Information

- Ensure that your input does not exceed the limits of integer data types.
- The program assumes that the input will be integers.
- The vectors will be sorted in ascending order.
