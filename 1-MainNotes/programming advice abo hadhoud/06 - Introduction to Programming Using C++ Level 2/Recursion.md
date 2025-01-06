# Recursive Functions in C++

A **recursive function** is a function that calls itself, either directly or indirectly, to solve a problem by breaking it down into smaller subproblems. Recursion is useful for problems that have a naturally repetitive or self-similar structure, such as factorials, Fibonacci sequences, and traversing trees.

---

## How Recursive Functions Work

1. **Base Case**:
    
    - Stops the recursion and prevents infinite loops.
    - Example: When computing factorial, the base case is when the input is `0`.
2. **Recursive Case**:
    
    - Reduces the problem to a smaller version of itself.
    - Example: In factorial, `n! = n * (n-1)!`.
3. **Unwinding**:
    
    - After reaching the base case, the function resolves each call step-by-step, combining results.

---

## Anatomy of a Recursive Function

```cpp
int factorial(int n) {
    if (n == 0) { // Base case
        return 1;
    }
    return n * factorial(n - 1); // Recursive case
}
```

### Explanation

- **Base Case**: If `n == 0`, the function returns `1` (stopping condition).
    
- **Recursive Case**: Multiplies `n` by the result of `factorial(n - 1)`.
    
- **Unwinding**: For `factorial(3)`, the calls look like:
    
    3×(2×(1×1))=63 \times (2 \times (1 \times 1)) = 6.
    

---

## Example: Power Function

```cpp
int power(int base, int exp) {
    if (exp == 0) { // Base case
        return 1;
    }
    return base * power(base, exp - 1); // Recursive case
}
```

### Explanation

- **Base Case**: Returns `1` when `exp == 0`.
- **Recursive Case**: Multiplies the `base` by the result of `power(base, exp - 1)`.

---

## Key Points to Remember

1. **Every recursion must have a base case** to avoid infinite loops.
2. Recursive functions use the **call stack**, which can lead to a stack overflow if the recursion depth is too large.
3. Tail recursion can optimize performance, but standard recursion is often simpler to write and understand.

---

## Common Use Cases

1. **Mathematical problems**: Factorials, Fibonacci, power calculations.
2. **Data structures**: Traversing trees, graphs, or recursive algorithms like quicksort and mergesort.
3. **Backtracking**: Solving mazes, puzzles like N-Queens, or generating permutations.