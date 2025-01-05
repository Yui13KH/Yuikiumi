# Header Files and Namespaces: A Simple Explanation

---

## **Header Files**

A header file in C++ is a file with a `.h` extension that contains declarations for functions, classes, constants, and other elements. The actual implementation of these declarations can be in a separate `.cpp` file. Header files allow you to:

- Reuse code across multiple files.
- Organize your program into smaller, manageable parts.

### **Example of a Header File (`math.h`):**

```cpp
#pragma once = // Prevents multiple inclusions=
namespace SimpleMath {
    int add(int a, int b);
    int subtract(int a, int b);
}
```

**Explanation:**

- `#pragma once`: Ensures the file is only included once during compilation.
- `SimpleMath` namespace: Groups related functions.

---

## **Namespaces**

Namespaces are used to organize code and avoid naming conflicts. For example, if two libraries define a function with the same name, using namespaces can help avoid collisions.

### **Example of a Namespace:**

```cpp
namespace SimpleMath {
    int add(int a, int b) {
        return a + b;
    }

    int subtract(int a, int b) {
        return a - b;
    }
}
```

**How to Use:**

- Access these functions with `SimpleMath::add` or `SimpleMath::subtract`.

---

## **How to Use Header Files in Another File**

To use the functions or declarations from a header file in another `.cpp` file, you need to include the header file using `#include`.

### **Example:**

#### **1. Header File (`math.h`):**


```cpp
#pragma once
namespace SimpleMath {
    int add(int a, int b);
    int subtract(int a, int b);
}
```


#### **2. Implementation File (`math.cpp`):**

```cpp
#include "math.h"

namespace SimpleMath {
    int add(int a, int b) {
        return a + b;
    }

    int subtract(int a, int b) {
        return a - b;
    }
}
```


#### **3. Main Program (`main.cpp`):**

```cpp
#include <iostream>
#include "math.h"

int main() {
    int a = 5, b = 3;

    std::cout << "Addition: " << SimpleMath::add(a, b) << "\n";
    std::cout << "Subtraction: " << SimpleMath::subtract(a, b) << "\n";

    return 0;
}
```

---

## **Key Points:**

- Use `#pragma once` or `#ifndef` guards to avoid multiple inclusions of a header file.
- Group related functions or classes in a `namespace` to prevent naming conflicts.
- Use `#include "file.h"` to import a header file into your program.