
tags : [[computer-science]] [[programming-foundations]] [[abu-hadhoud]]

### **Efficient Use of Data Types in C++**

#### **General Idea**

- Don’t memorize exact sizes or ranges of data types; instead, understand the general concept.
- Each type has a specific size and range based on the bytes it occupies in memory. For example:
    - Using `int` for something like an age variable is inefficient since the maximum age won’t exceed 150.

For reference, here's a table illustrating type ranges and sizes:  
![[Type Ranges and Sizes.png]]

---

### **Type Modifiers**

Type modifiers allow you to adjust the behavior of fundamental data types:

1. **Signed**
2. **Unsigned**
3. **Short**
4. **Long**

#### **Applicability**

Modifiers can be used with these types:

1. `int`
2. `double`
3. `char`

---

### **Signed vs. Unsigned**

- **Signed:** Supports both positive and negative values (default for most types).
- **Unsigned:** Shifts the range to only positive values.
    - Example: Use unsigned if negative values aren’t possible.

---

### **Short vs. Long**

- **Short:** Reduces the size of the type to save memory.
    - Example: A `short int` uses **2 bytes** instead of **4 bytes** for a normal `int`.
- **Long:** Increases the size and range of the type.

Here's a visual explanation:  
![[Int ranges and sizes.png]]

---

### **Questions**

1. **Can I use 1 byte if a number won’t exceed 256?**
    
    - Yes, you can use `unsigned char` to save memory.
2. **Can I use 7 bits for numbers like human age (max 128)?**
    
    - No, the minimum unit of storage in memory is 1 byte (8 bits).

---

### **Floating-Point Types**

- **Float, Double, Long Double:** Their sizes and ranges are shown here:  
    ![[float ranges and sizes.png]]
    
- **Unsigned Floats:** Not supported because floating-point storage differs fundamentally from integers.
    

---

### **Character Types**

- **Signed vs. Unsigned `char`:**
    - **Unsigned `char`:** Range is 0 to 255.
    - **Signed `char`:** Range is -128 to +127.

---

### **Note**

By default, all data types are **signed** unless specified otherwise.

