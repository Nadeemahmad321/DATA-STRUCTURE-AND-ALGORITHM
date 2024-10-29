# Unique Element Finder in Array

## Description

This program finds the unique element in an array where every other element appears twice. It utilizes the properties of the XOR bitwise operation, which is efficient for this specific problem.

## How It Works

The XOR operation has some interesting properties:
1. `a ^ a = 0` (any number XORed with itself is 0)
2. `a ^ 0 = a` (any number XORed with 0 is the number itself)
3. XOR is commutative and associative.

When you XOR all the numbers in the array, the pairs will cancel each other out, leaving only the unique number.

## Example

### Input
Enter the size of the array: 5 Enter the elements of the array: 2 3 5 3 2

shell
Copy code

### Output
Unique element in the array is: 5

markdown
Copy code

### Explanation
In the given input, the array consists of the numbers `2, 3, 5, 3, 2`. Here:
- `2` appears twice.
- `3` appears twice.
- `5` appears only once.

Using the XOR operation:
- `2 ^ 2 = 0`
- `3 ^ 3 = 0`
- `0 ^ 5 = 5`

Thus, the unique element is `5`.

## Complexity Analysis

- **Time Complexity**: O(n), where n is the number of elements in the array. This is because we traverse the array once.
- **Space Complexity**: O(1), as we are using a constant amount of extra space for the variable `ans`.

## Usage

1. Compile the code using a C++ compiler.
2. Run the executable.
3. Input the size and elements of the array as prompted.
4. The program will output the unique element.

## Important Notes

- This code assumes that there is exactly one unique element in the array, and all other elements appear in pairs.
- Ensure that the input size does not exceed the defined array limit (100 in this case).


### Example Input
```
Enter the size of the array: 5
Enter the elements of the array: 2 3 5 3 2
```

### Elements in the Array
The array can be represented as: `[2, 3, 5, 3, 2]`

### Step-by-Step Iteration Explanation

1. **Initialization**
   - Before starting the iterations, we initialize `ans` to `0`.

2. **Iteration 1: XOR with 2**
   - Current `ans`: `0`
   - Current element: `2`
   - Calculation: `ans = ans ^ 2 = 0 ^ 2 = 2`
   - Updated `ans`: `2`

3. **Iteration 2: XOR with 3**
   - Current `ans`: `2`
   - Current element: `3`
   - Calculation: `ans = ans ^ 3 = 2 ^ 3`
     - Binary representation:
       - `2` = `10`
       - `3` = `11`
     - XOR operation:
       - ```
         10
         11
         __
         01  (which is 1 in decimal)
         ```
   - Updated `ans`: `1`

4. **Iteration 3: XOR with 5**
   - Current `ans`: `1`
   - Current element: `5`
   - Calculation: `ans = ans ^ 5 = 1 ^ 5`
     - Binary representation:
       - `1` = `01`
       - `5` = `101`
     - XOR operation:
       - ```
         001
         101
         ____
         100  (which is 4 in decimal)
         ```
   - Updated `ans`: `4`

5. **Iteration 4: XOR with 3**
   - Current `ans`: `4`
   - Current element: `3`
   - Calculation: `ans = ans ^ 3 = 4 ^ 3`
     - Binary representation:
       - `4` = `100`
       - `3` = `011`
     - XOR operation:
       - ```
         100
         011
         ____
         111  (which is 7 in decimal)
         ```
   - Updated `ans`: `7`

6. **Iteration 5: XOR with 2**
   - Current `ans`: `7`
   - Current element: `2`
   - Calculation: `ans = ans ^ 2 = 7 ^ 2`
     - Binary representation:
       - `7` = `111`
       - `2` = `010`
     - XOR operation:
       - ```
         111
         010
         ____
         101  (which is 5 in decimal)
         ```
   - Updated `ans`: `5`

### Final Result
After processing all elements, the final value of `ans` is `5`. This value represents the unique element in the array, as all other elements (2 and 3) appeared in pairs and canceled each other out during the XOR operations.

### Conclusion
This step-by-step breakdown demonstrates how the XOR operation effectively identifies the unique element by exploiting its properties, resulting in an efficient solution with linear time complexity.
