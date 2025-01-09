
tags : [[foundations]]  [[data-representation]] [[abu-hadhoud]] [[binary-system]]

At its core, a computer is just billions of transistors acting as binary switches:

- **On (1)**: Electricity flows.
- **Off (0)**: No electricity.

Everything in a computer boils down to these binary states.

---

## Decimal vs. Binary

- **Decimal**: The number system humans use, based on 10 digits (0-9).
- **Binary**: The number system computers use, based on only two states: 0 and 1.

---

## What is a Bit?

- A **bit** is the smallest unit of information in computing.
- It has only two possibilities:
    - **1**: Electricity flows.
    - **0**: Electricity does not flow.

---

## What is a Byte?

- A **byte** is made up of **8 bits** and is the smallest unit of meaningful information.

### Binary Breakdown of a Byte

- **LSB (Least Significant Bit)**: The rightmost bit (2^0 = 1).
- **MSB (Most Significant Bit)**: The leftmost bit (2^7 = 128).

### Byte Value Range

- A single byte can represent numbers from **0 to 255** (base 2).

### Numbers Larger Than 255

- To represent numbers larger than 255, you need **more bytes**:
    - **2 bytes**: Starts at 2^8 (LSB) and goes up to 2^15 (MSB).
    - With 2 bytes, you can represent numbers up to **65,535**.

---

## ASCII (American Standard Code for Information Interchange)

- A standardized system for encoding English characters, assigning values to:
    - **Capital letters**.
    - **Lowercase letters**.
    - **Basic symbols**.

---

## Unicode (Universal Character Encoding Standard)

- A global standard for encoding characters from all languages and symbols.
- Created to represent every symbol, letter, and character ever used in any language.
- Essentially, some "insane people" decided to assign a unique value for **everything**.


