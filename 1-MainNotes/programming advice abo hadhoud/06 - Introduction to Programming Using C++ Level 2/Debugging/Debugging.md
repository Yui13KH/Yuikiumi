[[2-Tags/debugging]] [[abu-hadhoud]]
## Debugging: What Is It and Why Do We Need It?

Debugging is the process of identifying and fixing errors in your program. There are three main types of errors:

### 1. **Syntax Error**
   - **Definition:** These errors occur when the code is not written according to the syntax rules of the programming language. 
   - **Example:** Missing semicolons, incorrect parentheses, or misspelled keywords.
   - **Solution:** These are usually easy to fix because the compiler or interpreter will point them out.

### 2. **Logical Error**
   - **Definition:** These errors happen when the program runs, but it produces incorrect results. 
   - **Example:** Using the wrong formula, making incorrect assumptions, or not handling edge cases.
   - **Solution:** These can be tricky and require careful analysis, as the code runs without crashing, but it doesn't behave as expected.

### 3. **Runtime Error**
   - **Definition:** These errors occur during the execution of the program, causing it to crash or behave unexpectedly.
   - **Example:** Division by zero, accessing an out-of-bounds array element, or null pointer dereferencing.
   - **Solution:** These are harder to predict because they depend on the inputs or state of the program at runtime.

### Why Debugging is Important

Debugging helps programmers identify **logical errors** by tracking the flow of values and how they change during program execution. It involves using tools to stop the program at specific points where an issue might be occurring.

#### **Breakpoints**
- Breakpoints are special markers set in the code that pause execution at a certain line.
- This allows the programmer to inspect variable values in memory and step through the code line by line, even though C++ is a compiled language.

By using debugging tools effectively, you can trace and fix errors more efficiently, improving the reliability and performance of your code.


- **Step Into**: Go inside a function to inspect its code. usually *f11*
- **Step Over**: Execute a function as a whole without stepping inside. *f10*
- **Step Out**: Exit the current function and return to the caller. *shift f11*
