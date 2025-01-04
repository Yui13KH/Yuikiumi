
tags : [[abu-hadhoud]] , [[programming-foundations]] [[computer-science]]

---

### Decimal vs Hexadecimal vs Binary

#### **Decimal (Base 10)**

- Decimal is the standard number system, which uses **base 10**.
- It consists of digits from **0 to 9**.

#### **Binary (Base 2)**

- Binary uses **base 2**, meaning it only consists of **0s and 1s**.
- It is the foundational number system for computers since they use binary for data processing.

#### **Hexadecimal (Base 16)**

- Hexadecimal is a **base 16** system, combining **0-9** and **A-F** (where **A** = 10, **B** = 11, ..., **F** = 15).
- It is commonly used in computing, especially for representing colors in HTML/CSS, as it is easier to read and remember than long binary strings. For example, **#FFFFFF** (hexadecimal) is easier to remember than the corresponding binary value.

---

### **Converting Decimal to Hexadecimal**

Converting decimal numbers to hexadecimal is straightforward, essentially a process of repeated division by 16.

1. **Divide the number by 16.**
2. **Separate the result into the integer and fractional parts.**
3. **Multiply the fractional part by 16 to find the remainder.**
4. If the integer is greater than 16, continue dividing; otherwise, use the integer and remainder.
5. **Order the results** from last to first and convert to hexadecimal values (0-9, A-F).

#### Example: Converting 30 to Hexadecimal

1. **30 ÷ 16 = 1.875**
    - Integer: **1**, Fraction: **0.875**
2. **0.875 × 16 = 14**
    - Remainder: **14**, which corresponds to **E** in hexadecimal.
3. Since the integer is less than 16, we stop here.

**Result**: **1E**

---

### **Converting Hexadecimal to Decimal**

Converting hexadecimal to decimal is simpler. You start from the rightmost digit and multiply each digit by **16^x**, where **x** is the position of the digit (starting at 0).

#### Example: Converting **AE7** to Decimal

1. **7 × 16^0 = 7**
2. **E (value of 14) × 16^1 = 224**
3. **A (value of 10) × 16^2 = 2560**

**Result**: **7 + 224 + 2560 = 2791**

---

### **Hexadecimal to Binary Conversion**

There are two ways to convert hexadecimal to binary:

#### **Method 1: Via Decimal**

1. Convert the hexadecimal value to decimal.
2. Then, convert the decimal value to binary.

---

#### **Method 2: Direct Conversion Using Nibbles**

- Hexadecimal digits can be directly converted to binary by treating each digit as a **4-bit nibble**:
    1. Split the hexadecimal number into individual digits.
    2. Convert each hex digit into its **4-bit binary equivalent**.
    3. Combine the binary nibbles to get the final binary result.

**Example: Convert `AE` to Binary**

1. Split `AE` into its hex digits:
    - `A` = **10** in decimal
    - `E` = **14** in decimal
2. Convert each to a 4-bit binary nibble:
    - `A` = **1010**
    - `E` = **1110**
3. Combine the binary nibbles:
    - Result = **1010 1110**

This method is quicker and avoids intermediate decimal conversion!

---