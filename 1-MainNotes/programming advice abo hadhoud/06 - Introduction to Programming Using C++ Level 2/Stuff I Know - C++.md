# Ternary Operator

The **ternary operator** is a shorthand for `if-else` that evaluates a condition and returns one of two values.

### Syntax:
`condition ? value_if_true : value_if_false;`

### Example:
```cpp
int max = (a > b) ? a : b; // Returns 'a' if a > b, otherwise 'b'

```

---
# Range-based Loop

Simplifies iterating over a container in C++.

### Syntax:
```cpp
for (element_type element : container) {
    // Use element
}
```

```cpp
int numbers[] = {1, 2, 3, 4, 5};

for (int num : numbers) {
    std::cout << num << " ";
}
// Output: 1 2 3 4 5

```


---

# Bitwise Operations and Shifts in C++ 
## 1. Bitwise AND (`&`) 

The **bitwise AND** operation compares each corresponding bit of two numbers and returns `1` if both bits are `1`; otherwise, it returns `0`. 

**Example:** 

```cpp
int a = 5;   // Binary: 0101 
int b = 3;   // Binary: 0011 
int result = a & b;  // Binary: 0001 (1)
```

---
## 2. Bitwise OR (`|`)

The **bitwise OR** operation compares each corresponding bit of two numbers and returns `1` if at least one bit is `1`; otherwise, it returns `0`.

**Example:**

```cpp
int a = 5;   // Binary: 0101 
int b = 3;   // Binary: 0011 
int result = a | b;  // Binary: 0111 (7)
```

---

## 3. Bitwise XOR (`^`)

The **bitwise XOR** (exclusive OR) operation compares each corresponding bit of two numbers and returns `1` if the bits are different, otherwise it returns `0`.

```cpp
int a = 5;   // Binary: 0101 
int b = 3;   // Binary: 0011 
int result = a ^ b;  // Binary: 0110 (6)
```

---

## 4. Bitwise NOT (`~`)

The **bitwise NOT** operation inverts the bits of a number. It flips `0` to `1` and `1` to `0`.


```cpp
int a = 5;    // Binary: 0101 
int result = ~a;  // Binary: 1010 (in 2's complement: -6)
```

---
## 5. Left Shift (`<<`)

The **left shift** operation shifts all the bits of a number to the left by a specified number of positions. This effectively multiplies the number by `2^n`, where `n` is the number of positions.


```cpp
int a = 5;   // Binary: 0101 
int result = a << 2;  // Binary: 10100 (20)
```

---
## 6. Right Shift (`>>`)

The **right shift** operation shifts all the bits of a number to the right by a specified number of positions. This effectively divides the number by `2^n`, where `n` is the number of positions.

```cpp
int a = 5;   // Binary: 0101 
int result = a >> 1;  // Binary: 0010 (2)
```

---
## 7. XOR Swap Trick

You can swap two variables using the **XOR** operator without a temporary variable. This works due to the reversible property of XOR.

```cpp
x ^= y;   
y ^= x;   
x ^= y;
```

**Explanation:**

- `x ^= y` stores `x ^ y` in `x`.
- `y ^= x` stores the original value of `x` in `y`.
- `x ^= y` then stores the original value of `y` in `x`.

## Use Cases

- **Bitwise AND**: Used for masking (selecting certain bits).
- **Bitwise OR**: Used for setting specific bits.
- **Bitwise XOR**: Used for toggling bits and performing certain cryptographic operations.
- **Bitwise NOT**: Used for inverting bits.
- **Bit Shifts**: Used for fast multiplication or division by powers of two.

## Performance Considerations

- Bitwise operations are often faster than their arithmetic counterparts, especially when manipulating individual bits or flags.
- Using bitwise shifts for multiplication and division by powers of two is a common optimization.