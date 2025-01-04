

---

### **Breakpoints**

- **Definition**: A breakpoint is a marker placed on a specific line of code to pause program execution during debugging.
- **Purpose**:
    - Helps examine program state at specific points.
    - Identifies issues such as logical errors or unexpected behavior.
- **How It Works**:
    - When the program reaches a breakpoint, the debugger halts execution.
    - The debugger allows stepping through the code line by line or inspecting variable values and memory.
- **Types of Breakpoints**:
    - **Standard Breakpoint**: Pauses at a specific line.
    - **Conditional Breakpoint**: Pauses only when a specified condition evaluates to true.
    - **Function Breakpoint**: Pauses execution when a particular function is called.
    - **Watchpoint**: Monitors changes in a variable's value.
- **Tips**:
    - Place breakpoints near areas where you suspect bugs.
    - Use conditional breakpoints to save time by pausing only on relevant conditions.

---
I like how a quick search on wiki gives more info 


### **Memory Values**

- **Definition**: Memory values are the raw data stored in your computer's memory (RAM) during program execution.
- **Uninitialized Variables**:
    - Variables declared but not initialized can hold unpredictable "garbage" values.
    - The behavior of uninitialized variables depends on the compiler and environment.
- **Inspecting Memory**:
    - During debugging, you can inspect raw memory values in **hexadecimal** or **binary**.
    - Memory inspection can reveal the content of pointers, arrays, or dynamically allocated memory.
- **Registers**:
    - The CPU uses registers like `RAX`, `RBX`, and `RCX` to store intermediate values.
    - Debuggers often show register values, which can help identify low-level issues.
- **Breakpoints and Memory**:
    - Use breakpoints to pause execution and check how memory values change step by step.
    - Debuggers let you watch specific memory addresses or variable locations in memory.
- **Tips**:
    - Be cautious of accessing memory outside allocated bounds (undefined behavior).
    - Use tools like address sanitizers or valgrind to detect memory issues.

---
