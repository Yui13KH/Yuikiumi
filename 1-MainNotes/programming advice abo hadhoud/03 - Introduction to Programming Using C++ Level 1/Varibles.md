tags : [[programming]] [[programming-foundations]] [[abu-hadhoud]]

### **Data Types in C++**

C++ data types are classified into three categories:

1. **Fundamental Data Types**
2. **Derived Data Types**
3. **User-Defined Data Types**

---

#### **1. Fundamental Data Types**

These are the basic built-in types provided by C++:

- **Integral Types**:
    
    - `int`: Whole numbers (e.g., `19`)
    - `char`: Single character (e.g., `"A"`, uses ASCII encoding, not the actual character)
- **Floating Types**:
    
    - `float`: Floating-point numbers with single precision (e.g., `14.5`)
    - `double`: Floating-point numbers with double precision (larger than `float`)
- **Boolean Type**:
    
    - `bool`: Can hold `true` or `false`
- **String Type**:
    
    - `string`: Represents text (e.g., `"yui"`)
- **Void Type**:
    
    - `void`: Represents an empty or null type (used for functions with no return value)
- **Wide Character Type**:
    
    - `wchar_t`: Stores Unicode characters (e.g., for internationalization)

---

#### **2. Derived Data Types**

These types are built from fundamental types:

- **Function**: A block of code that performs a specific task.
- **Array**: A collection of elements of the same type.
- **Pointer**: A variable that stores the memory address of another variable.
- **Reference**: An alias for another variable, which allows indirect access to it.

---

#### **3. User-Defined Data Types**

These are types created by the programmer:

- **Class**: A blueprint for creating objects (encapsulates data and functions).
- **Structure**: Similar to a class, but typically used for grouping different data types together.
- **Union**: Allows storing different data types in the same memory location.
- **Enum**: A set of named integer constants.
- **Type Def**: Creates a new type alias for an existing type.

---

### **Declaring Variables**

The syntax for declaring a variable is:

cpp

Copy code

`type variableName = value;`

- You don't need to assign a value immediately; you can assign it later. For example:

cpp

Copy code

`int x;  // Declaration without initialization x = 5;  // Assign value later`

- You can reassign values to variables as needed.

---

### **Constants**

A **constant** is a variable whose value cannot be changed after initialization.

- **Syntax**:
    
    cpp
    
    Copy code
    
    `const type variableName = value;`
    
- If you try to change its value later, it will throw an error.