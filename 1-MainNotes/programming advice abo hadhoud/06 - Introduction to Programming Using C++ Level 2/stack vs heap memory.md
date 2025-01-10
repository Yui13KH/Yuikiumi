
---

### **Tags**: [[abu-hadhoud]], [[memory-management]]

According to the instructor's video, when you run a program, the memory is allocated in the following order:

1. **Source Code / Instructions**
    
    - This is the part of memory where the compiled code (machine instructions) resides. The processor reads and executes these instructions.
2. **Static / Global Memory**
    
    - This section holds static and global variables that exist for the entire lifetime of the program. These variables are allocated when the program starts and are deallocated when the program exits.
3. **Stack Memory**
    
    - The stack is used for **local variables**, function calls, and **function parameters**. It's managed in a **Last In, First Out (LIFO)** order, meaning that the most recent function call will have its local variables stored on top.
    - The stack is also used for **pointers** (though the memory they point to might reside in the heap).
4. **Heap Memory**
    
    - The heap is used for **dynamically allocated memory**, such as objects, arrays, and variables created at runtime. This memory is manually managed by the programmer, typically through the use of **pointers** (using `new`, `delete`, etc.).
    - The heap provides **more flexible memory allocation** than the stack, since the stack has a fixed size that the compiler determines before the program runs. The heap, on the other hand, allows you to request memory dynamically during the program's execution, so you can allocate more memory if needed.

---

### **Pointers and Heap Memory**:

- **Pointers** allow you to access and manipulate memory in the heap. The stack memory has a predefined size, but with pointers, you can request additional memory on the heap at runtime, beyond what was initially allocated by the compiler.
- This flexibility is essential for working with large data structures like dynamically sized arrays, objects, or even entire programs that need to manage memory efficiently during execution.

In summary, **pointers** provide the means to extend the memory usage beyond the compiler’s initial estimate, giving you the ability to dynamically allocate and manage memory on the heap when needed.

---
