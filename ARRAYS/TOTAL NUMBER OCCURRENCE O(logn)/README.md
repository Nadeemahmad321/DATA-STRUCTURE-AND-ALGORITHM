# Total Number of Occurrences in a Sorted Array

## Description

This C++ program calculates the total number of occurrences of a specified key in a sorted array. It uses binary search techniques to efficiently find both the first and last occurrences of the key, resulting in a time complexity of \( O(\log n) \).

## Features

- Finds the first occurrence of a key in a sorted array.
- Finds the last occurrence of a key in a sorted array.
- Calculates the total number of occurrences of the key.

## Functions

### 1. `firstOccurrence`

```cpp
int firstOccurrence(const vector<int>& arr, int key);
```
- **Parameters**: 
  - `arr`: A sorted vector of integers.
  - `key`: The integer to search for.
- **Returns**: The index of the first occurrence of the key, or -1 if not found.

### 2. `lastOccurrence`

```cpp
int lastOccurrence(const vector<int>& arr, int key);
```
- **Parameters**:
  - `arr`: A sorted vector of integers.
  - `key`: The integer to search for.
- **Returns**: The index of the last occurrence of the key, or -1 if not found.

### 3. `totalNumberOfOccurrence`

```cpp
int totalNumberOfOccurrence(const vector<int>& arr, int key);
```
- **Parameters**:
  - `arr`: A sorted vector of integers.
  - `key`: The integer to search for.
- **Returns**: The total number of occurrences of the key in the array.

## Complexity

- **Time Complexity**: \( O(\log n) \) for both finding the first and last occurrences.
- **Space Complexity**: \( O(1) \) since we are using a constant amount of space.

## Usage

1. Compile the program using a C++ compiler.
2. Run the executable.
3. Input the size of the vector.
4. Input the elements of the vector.
5. Input the key you wish to search for.
6. The program will output the total number of occurrences of the key.

## Example with Step-by-Step Solution

### Input
```
Enter the size of vector: 7
Enter the elements of vector: 1 2 2 2 3 4 5
Enter the key: 2
```

### Step-by-Step Breakdown

1. **Finding the First Occurrence**:
   - Start with `start = 0`, `end = 6` (size of array - 1).
   - Calculate `mid = (0 + 6) / 2 = 3`. `arr[3] = 2`.
   - Since `arr[3] == key`, record `ans = 3` and search left: `end = mid - 1 = 2`.
   - New `mid = (0 + 2) / 2 = 1`. `arr[1] = 2`.
   - Since `arr[1] == key`, record `ans = 1` and search left: `end = mid - 1 = 0`.
   - New `mid = (0 + 0) / 2 = 0`. `arr[0] = 1`.
   - Since `arr[0] < key`, search right: `start = mid + 1 = 1`.
   - `start` is now greater than `end`, so the first occurrence is at index `1`.

2. **Finding the Last Occurrence**:
   - Reset `start = 0`, `end = 6`.
   - Calculate `mid = (0 + 6) / 2 = 3`. `arr[3] = 2`.
   - Since `arr[3] == key`, record `ans = 3` and search right: `start = mid + 1 = 4`.
   - New `mid = (4 + 6) / 2 = 5`. `arr[5] = 4`.
   - Since `arr[5] > key`, search left: `end = mid - 1 = 4`.
   - New `mid = (4 + 4) / 2 = 4`. `arr[4] = 3`.
   - Since `arr[4] > key`, search left: `end = mid - 1 = 3`.
   - `start` is now greater than `end`, so the last occurrence is at index `3`.

3. **Calculating Total Occurrences**:
   - Total occurrences = (last - first) + 1 = (3 - 1) + 1 = 3.

### Output
```
Total number of occurrences: 3
```

## Important Information

- The array must be sorted for the binary search to work correctly.
- The program handles cases where the key is not present in the array, returning `0` occurrences.
- This method is efficient for large datasets due to its logarithmic time complexity.

