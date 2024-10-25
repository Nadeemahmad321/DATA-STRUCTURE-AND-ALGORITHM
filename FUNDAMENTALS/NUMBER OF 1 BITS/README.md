# Number of 1 Bits

This C++ program counts the number of bits that are set to `1` in the binary representation of a given integer. This is also known as the Hamming weight or population count.

## Brief Explanation

The program works by utilizing bitwise operations to efficiently determine how many bits are `1`. Here are the key components:

1. **Input**: The user is prompted to enter an integer.

2. **Counting Function (`countOnes`)**:
   - A loop iterates as long as the number is not zero.
   - The expression `(n & 1)` checks if the least significant bit of `n` is `1`. If true, the counter is incremented.
   - The right shift operation `n = n >> 1` moves all bits of `n` one position to the right, effectively discarding the bit just checked.

3. **Output**: After processing all bits, the program outputs the total count of `1` bits.

## Code

```cpp
#include <iostream>
using namespace std;

int countOnes(int n) {
    int count = 0;
    while (n != 0) {
        // Check if the least significant bit is 1
        if (n & 1) {
            count++;
        }
        // Right shift to check the next bit
        n = n >> 1;
    }
    return count;
}

int main() {
    int n;
    cout << "Enter the number: ";
    cin >> n;

    int count = countOnes(n);
    cout << "Number of 1 bits is: " << count;
    return 0;
}
```

## Usage

1. Compile the program using a C++ compiler:
   ```bash
   g++ -o count_ones count_ones.cpp
   ```

2. Run the executable:
   ```bash
   ./count_ones
   ```

3. Enter an integer when prompted, and the program will display the number of `1` bits.

## Example

### Input:
```
Enter the number: 5
```

### Output:
```
Number of 1 bits is: 2
```


# important 
### What is Bitwise AND?

1. **Bitwise Operator**: The `&` operator is called the bitwise AND operator. It compares each corresponding bit of two numbers and returns a new number.
   
2. **Comparison**:
   - For each pair of bits (from the two numbers), the result is:
     - `1` if both bits are `1`
     - `0` if either bit is `0`
   
### How It Works with `(number & 1)`

- **Binary Representation**: Every integer can be represented in binary (base 2). The least significant bit (LSB) is the rightmost bit in this representation.

- **Number 1 in Binary**: The number `1` in binary is represented as `...0001`, where all bits to the left of the rightmost `1` can be either `0` or `1`.

- **Effect of `(number & 1)`**:
  - When you perform `number & 1`, you're effectively isolating the LSB of `number`.
  - If the LSB is `1`, the result of the operation will be `1`.
  - If the LSB is `0`, the result will be `0`.

### Example

Let's say `number` is `6`. The binary representation of `6` is `110`.

- Binary:
  ```
  number:  110  (6 in decimal)
  1:       001  (1 in decimal)
  -----------------
  result:  000  (0 in decimal)
  ```

Now, if `number` is `5`, which is `101` in binary:

- Binary:
  ```
  number:  101  (5 in decimal)
  1:       001  (1 in decimal)
  -----------------
  result:  001  (1 in decimal)
  ```

### Conclusion

- **Purpose**: The `(number & 1)` operation is a quick and efficient way to check whether the number is odd or even:
  - If the result is `1`, the number is odd.
  - If the result is `0`, the number is even.

In the context of the function we discussed earlier, this operation helps to count how many bits are set to `1` in the binary representation of `number`. Each time `(number & 1)` returns `1`, it indicates that the current bit being checked is a `1`, so the count is incremented. Then, `number` is right-shifted (`number >>= 1`) to check the next bit in the subsequent iteration.
