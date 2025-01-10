### **Tags**: [[abu-hadhoud]], [[memory-management]]

---

### **Dynamic Memory Allocation Using Pointers in C++**

Pointers allow you to dynamically allocate memory during runtime. This gives you flexibility to create variables, use them, and release the memory when you're done to avoid memory leaks.

---

#### **Example: Allocating and Deallocating Memory**

```cpp
#include <iostream>
using namespace std;

int main() {
    // Declare pointers for int and float
    int* ptrX;    // Pointer to an integer
    float* ptrY;  // Pointer to a float

    // Dynamically allocate memory for these variables
    ptrX = new int;
    ptrY = new float;

    // Assign values to the dynamically allocated variables
    *ptrX = 10;
    *ptrY = 10.5f;

    // Use the allocated memory
    cout << "Value of ptrX: " << *ptrX << endl;
    cout << "Value of ptrY: " << *ptrY << endl;

    // Deallocate the memory to avoid memory leaks
    delete ptrX;
    delete ptrY;

    return 0;
}
```

---

#### **Key Notes:**

1. **Dynamic Allocation**:
    
    - Use `new` to allocate memory dynamically.
    - This is useful when the size or number of variables isn’t known at compile time.
2. **Dereferencing Pointers**:
    
    - Use `*ptr` to access or modify the value stored in the memory address that `ptr` points to.
3. **Deallocating Memory**:
    
    - Always pair `new` with `delete` to free allocated memory.
    - Forgetting to `delete` allocated memory results in a **memory leak**.
4. **Null Pointers**:
    
    - After deallocating memory, set the pointer to `nullptr` to avoid dangling pointers.  
        Example:
    
    ```cpp
    delete ptrX;
    ptrX = nullptr;
    ```
    
5. **Avoid Common Mistakes**:
    
    - Deleting the same pointer twice can cause undefined behavior.
    - Accessing memory after deallocation is also undefined behavior.


---

## **Dynamic Arrays in C++**

In C++, pointers allow you to dynamically allocate memory for arrays at runtime. This is particularly useful when the size of the array is not known at compile time, and you need to allocate memory based on user input or other factors.

### **Example: Dynamic Array for Storing Ages**

```cpp
    int num = 0;

    cout << "Enter the number of users: ";
    cin >> num;

    // Dynamically allocate memory for the array
    int* ptrX = new int[num]; // Pointer to int, dynamically allocated array

    cout << "Enter ages of users:" << endl;
    for (int i = 0; i < num; i++) {
        cout << "User " << i + 1 << ": ";
        cin >> *(ptrX + i); // Using pointer arithmetic to store value
    }

    cout << "\nDisplaying ages of users:" << endl;
    for (int i = 0; i < num; i++) {
        cout << "User " << i + 1 << ": " << *(ptrX + i) << endl;
    }

    // Deallocate the dynamically allocated memory
    delete[] ptrX;  // Use delete[] for arrays
    ptrX = nullptr;  // Set pointer to nullptr for safety
```

### **Key Points:**

- **Dynamic Allocation**: We used `new` to allocate an array of integers (`new int[num]`), where `num` is the size determined by user input.
- **Pointer Arithmetic**: We accessed array elements using pointer arithmetic (`*(ptrX + i)`), which is equivalent to `ptrX[i]`.
- **Memory Deallocation**: It’s crucial to free dynamically allocated memory using `delete[]` when it's no longer needed, to avoid memory leaks. After deleting, we set the pointer to `nullptr` for safety.

### **Important Considerations:**

- **Array Size**: The array size must be known at runtime (user input, for example). In contrast, arrays declared statically (e.g., `int arr[10];`) have fixed sizes determined at compile time.
- **Memory Management**: Always ensure you free memory using `delete[]` to avoid memory leaks. Setting the pointer to `nullptr` afterward helps prevent potential issues when trying to access the pointer again.

---
