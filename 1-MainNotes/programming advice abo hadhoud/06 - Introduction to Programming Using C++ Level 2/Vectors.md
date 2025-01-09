tags : [[abu-hadhoud]] [[cpp]] [[advanced]]
# Vectors in C++

In physics, vectors are often used to represent quantities that have both magnitude and direction (such as forces). In C++, vectors can be treated as dynamic arrays that can grow or shrink in size. Below is a breakdown of how to use vectors effectively in C++.

## 1. **Including the Vector Library**

To use vectors in C++, you need to include the `vector` library:

```cpp
#include <vector>
```

## 2. **Declaring a Vector**

You can declare a vector as follows:

```cpp
std::vector<int> vName; // Declares a vector of integers
```

- You can also initialize a vector with values directly:

```cpp
std::vector<int> vName = {10, 20, 30}; // Initializes a vector with values
```

- Alternatively, you can declare an empty vector and add elements later:

```cpp
std::vector<int> vName; // Empty vector
vName.push_back(10); // Adds a value to the vector
```

---

## 3. **Looping Over a Vector**

### Using Range-based For Loop

You can loop over a vector using a range-based for loop:

```cpp
for (int i : vName) {
    // Do something with i
}
```

> **Note**: This loop creates a copy of each element in the vector, which may impact performance with large vectors. To avoid copying and make the code more efficient, you can use a reference:

```cpp
for (int &i : vName) {
    // Modify elements directly
}
```

This allows you to modify the vector elements **in place** without copying them.

---

## 4. **Working with Vectors of Structures**

You can store structures in a vector. First, define a structure and then declare a vector of that type:

```cpp
struct Point {
    int x, y;
};

std::vector<Point> points;
points.push_back({1, 2}); // Adds a Point structure to the vector
```

---

## 5. **Common Vector Operations**

- **Adding Elements:**
    
    - Use `push_back()` to add an element to the end of the vector:
    
    ```cpp
    vName.push_back(40); // Adds 40 to the end of vName
    ```
    
- **Removing Elements:**
    
    - `pop_back()` removes the last element:
    
    ```cpp
    vName.pop_back(); // Removes the last element
    ```
    
    - To remove all elements, use `clear()`:
    
    ```cpp
    vName.clear(); // Removes all elements from the vector
    ```
    
- **Accessing Elements:**
    
    - `vName.size()` returns the number of elements in the vector:
    
    ```cpp
    std::cout << "Size: " << vName.size() << std::endl;
    ```
    
    - `vName.front()` gives the first element and `vName.back()` gives the last element:
    
    ```cpp
    std::cout << "First: " << vName.front() << std::endl;
    std::cout << "Last: " << vName.back() << std::endl;
    ```
    
- **Capacity:**
    
    - `vName.capacity()` returns the current allocated memory for the vector (this may not be the same as the size of the vector):
    
    ```cpp
    std::cout << "Capacity: " << vName.capacity() << std::endl;
    ```
    

---

## 6. **Additional Notes**

- **Dynamic Size:** A vector’s size can change at runtime, unlike arrays, which have a fixed size. You don’t need to specify a size when declaring a vector.
- **Efficiency Considerations:** Using references (`&`) in loops and operations can significantly improve the performance of vector manipulations, especially for large data sets.

---
