tags : [[abu-hadhoud]] [[cpp]] [[advanced]]]]

# Declaration vs Definition in C++

## Definition
A **definition** provides the full implementation of a function, including its body. It tells the program what the function **does**.

**Example:**

```cpp
void printArray(int arr[], int size) {
    for (int i = 0; i < size; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;
}
```

## Declaration

A **declaration** is like a lookup address for the function. It tells the compiler that the function **exists** somewhere in the project, without providing its implementation. This is useful in C++ because it's a compiled language, and calling a function before it’s defined causes a compiler error.

```cpp
void printArray(int arr[], int size);
```

The **declaration** lets the compiler know about the function’s existence, so it can compile calls to `printArray` even if its definition is placed later in the file.

### Key Points About Declarations:

1. You don't need to include parameter names in the declaration:

    ```cpp
void printArray(int, int);
```
    
    The compiler only needs the **types** to understand the function signature.
    
2. Declarations are often placed:
    
    - At the top of the file (before `main()`).
    - In a header file (`.h`) to share them across multiple files.

---

## Why Use Declarations?

- **Order Independence**: Allows you to call a function before its definition.
- **Code Modularity**: Function declarations in header files make it easier to organize large projects.

---

## Summary

- **Definition**: Includes the function's body and logic (what it does).
- **Declaration**: States the function’s signature and existence (what it is).


---

# Default Parameters in Functions

**Default parameters** allow you to specify default values for function arguments. If no value is provided during the function call, the default value is used.

**Syntax:**
```cpp
void greet(string name = "Guest") { // default perameter 
    cout << "Hello, " << name << "!" << endl;
}
```

```cpp
greet();            // Outputs: Hello, Guest!
greet("Alice");     // Outputs: Hello, Alice!
```

---

# Function Overloading

**Function overloading** allows you to define multiple functions with the **same name** but **different parameter lists**. The compiler determines which function to call based on the arguments provided.

**Rules for Overloading:**
1. Functions must differ in:
   - Number of parameters.
   - Types of parameters.
   - Order of parameters.
2. Return type **cannot** be the sole criterion for overloading.

**Example:**
```cpp
#include <iostream>
using namespace std;

// Overloaded functions
void display(int num) {
    cout << "Integer: " << num << endl;
}

void display(double num) {
    cout << "Double: " << num << endl;
}

void display(string text) {
    cout << "String: " << text << endl;
}

int main() {
    display(5);            // Calls the integer version
    display(3.14);         // Calls the double version
    display("Hello!");     // Calls the string version
    return 0;
}
```

**Why Use Function Overloading?**

- Increases code readability by using the same name for similar operations.
- Simplifies function calls when dealing with multiple data types or parameter variations.


---

# Function Stack / Hierarchy in C++

The **function stack** refers to the mechanism by which functions are called, executed, and returned during a program’s runtime. The stack maintains the hierarchy of function calls, ensuring proper execution and cleanup.

---

## Key Concepts

### 1. **Call Stack**
- A **call stack** is a data structure that keeps track of function calls in a Last-In-First-Out (LIFO) manner.
- Each function call pushes a **stack frame** onto the stack.
- When a function returns, its stack frame is popped off.

### 2. **Stack Frame**
- A **stack frame** contains:
  - Function parameters.
  - Local variables.
  - Return address (where the program should return after the function finishes).
- Each function call has its own stack frame.

### 3. **Hierarchy**
- Functions are executed in a hierarchical order:
  1. The **main()** function is the root.
  2. Any function called by `main()` is added to the stack.
  3. Nested function calls form a tree-like hierarchy.

---

## Example: Function Call Hierarchy

**Code:**

```cpp
#include <iostream>
using namespace std;

void funcC() {
    cout << "In funcC()" << endl;
}

void funcB() {
    cout << "In funcB()" << endl;
    funcC(); // funcC is called here
}

void funcA() {
    cout << "In funcA()" << endl;
    funcB(); // funcB is called here
}

int main() {
    cout << "In main()" << endl;
    funcA(); // funcA is called here
    return 0;
}
```

**Execution Flow:**

1. `main()` calls `funcA()`.
    - Stack: `main → funcA`.
2. `funcA()` calls `funcB()`.
    - Stack: `main → funcA → funcB`.
3. `funcB()` calls `funcC()`.
    - Stack: `main → funcA → funcB → funcC`.
4. `funcC()` completes and returns to `funcB()`.
5. `funcB()` completes and returns to `funcA()`.
6. `funcA()` completes and returns to `main()`.

## Importance of Function Stack

- **Memory Management:** Each function has its own isolated memory (stack frame) for local variables.
- **Error Detection:** Stack overflow occurs if the stack exceeds its memory limit (e.g., infinite recursion).
- **Debugging:** Call stacks help trace the sequence of function calls during runtime.

## Summary

The function stack is a critical part of program execution, maintaining the order of function calls and ensuring the proper flow of control and memory isolation for each function.

---
