# Constructor Overloading in C++

##  Overview
- **Constructor Overloading** in C++ means defining **multiple constructors** in the same class with **different parameter lists** (number or type of parameters).  
- The compiler decides which constructor to call at runtime based on the arguments passed during object creation.  
- This provides **flexibility** in initializing objects in different ways.  

---

##  Theory

### What is a Constructor?
- A special member function of a class that is automatically called when an object is created.  
- It has the same name as the class and does not return a value.  

### Why Overload Constructors?
- To allow different ways of initializing objects.  
- Example: Sometimes you may want to initialize an object with default values, other times with user-provided values.  

### Rules of Constructor Overloading
- Constructors must have the same name as the class.  
- They must differ in the **number** or **type** of parameters.  
- The compiler selects the appropriate constructor using **function overloading rules**.  

---

# Operator Overloading in C++

##  Theory

### What is Operator Overloading?
- **Operator overloading** is a feature in C++ that allows developers to **redefine the meaning of operators** (`+`, `-`, `*`, `==`, `++`, etc.) for **user-defined data types (classes/objects)**.  
- It enables objects to be manipulated using operators just like primitive data types.  

For example:  
- Normally, `+` adds integers or floats.  
- With operator overloading, we can make `+` add two objects (e.g., two complex numbers).  

---

##  Key Points
1. Operator overloading is a type of **compile-time polymorphism**.  
2. It allows more **readable and natural code** for user-defined classes.  
3. Only **existing operators** can be overloaded; **new operators cannot** be created.  
4. Certain operators **cannot be overloaded** (e.g., `::`, `.`, `.*`, `sizeof`, `?:`).  
5. Operator overloading can be done using **member functions** or **friend functions**.  

---

##  Syntax

```cpp
class ClassName {
public:
    // Operator function
    returnType operator op (argument) {
        // operator definition
    }
};
```

# Function Overloading in C++

##  Theory

### What is Function Overloading?
- **Function Overloading** in C++ is a feature that allows **multiple functions with the same name** to exist in the same scope but with **different parameter lists**.  
- The compiler decides which function to invoke at **compile time** based on:
  - The **number of parameters**  
  - The **types of parameters**  
  - The **order of parameters**  
This makes the program more **flexible, readable, and reusable**.

---

##  Key Points
1. Function overloading is a form of **compile-time polymorphism**.  
2. Functions must differ in their **parameter list** (number, type, or order).  
3. The **return type alone** cannot differentiate overloaded functions.  
4. It allows using the same function name for different tasks, improving **code readability**.  

---

#  Program Summary

##  1. Adding two numbers using Constructor Overloading
- This program demonstrates **Constructor Overloading** in C++.  
- A class `Add` is created with **two constructors**:
  1. One constructor takes **three integer parameters** and computes their sum.  
  2. Another constructor takes **two integer parameters** and computes their sum.  
- When an object is created, the compiler automatically calls the constructor that matches the number of arguments passed.  
- This shows how **constructor overloading** provides flexibility in object initialization.  

---

##  Algorithm
1. **Start** the program.  
2. Define a class `Add` with:
   - A private data member `sum` of type `double`.  
   - A constructor that takes **three integers** (`a, b, c`), adds them, stores the result in `sum`, and prints it.  
   - A constructor that takes **two integers** (`a, b`), adds them, stores the result in `sum`, and prints it.  
3. In the `main()` function:  
   - Create object `A1` with three values `(25, 8500, 1000)`.  
     - This calls the **3-parameter constructor** → computes and prints the sum.  
   - Create object `A2` with two values `(5, 10)`.  
     - This calls the **2-parameter constructor** → computes and prints the sum.  
4. **End** the program.  

---

## 2. Constructor Overloading
- This program defines a class **Employee** that demonstrates **constructor overloading**.  
- The class has three private data members:
  - `name` (string)  
  - `age` (int)  
  - `salary` (double)  
- Multiple constructors are provided:
  1. **Default constructor** → initializes members with default values.  
  2. **One-parameter constructor** → initializes only the name.  
  3. **Two-parameter constructor** → initializes name and age.  
  4. **Three-parameter constructor** → initializes name, age, and salary.  
- The `displayDetails()` function prints employee details.  
- In `main()`, different employees are created using different constructors, showing the **flexibility of constructor overloading**.

---

##  Algorithm
1. **Start** the program.  
2. Define the `Employee` class with:
   - Private members: `name`, `age`, `salary`.  
   - Four overloaded constructors:
     - No parameters → default values.  
     - One parameter (name).  
     - Two parameters (name, age).  
     - Three parameters (name, age, salary).  
   - A member function `displayDetails()` to print employee info.  
3. In `main()`:  
   - Create object `emp1` with no parameters → calls default constructor.  
   - Create object `emp2("Mahi")` → calls one-parameter constructor.  
   - Create object `emp3("Palak", 30)` → calls two-parameter constructor.  
   - Create object `emp4("Pal", 40, 50000.0)` → calls three-parameter constructor.  
   - Display details of all employees using `displayDetails()`.  
4. **End** the program.  

---

## 3. Function Overloading
- This program demonstrates **Function Overloading** in C++.  
- A class `Shape` is created with three **overloaded functions** named `calculateVolume()`:
  1. `calculateVolume(double side)` → Calculates volume of a cube.  
  2. `calculateVolume(double length, double width, double height)` → Calculates volume of a rectangular prism.  
  3. `calculateVolume(double radius, double Height)` → Calculates volume of a cylinder.  
- Function overloading allows using the **same function name** with different **parameter lists**, improving readability and reusability.

---

##  Algorithm
1. **Start** the program.  
2. Define a class `Shape` with three overloaded `calculateVolume()` functions:
   - One parameter → cube volume.  
   - Three parameters → rectangular prism volume.  
   - Two parameters → cylinder volume.  
3. In the `main()` function:  
   - Call `calculateVolume(side)` to compute cube volume.  
   - Call `calculateVolume(length, width, height)` to compute rectangular prism volume.  
   - Call `calculateVolume(radius, Height)` to compute cylinder volume.  
4. Print all calculated volumes.  
5. **End** the program.  

---

## 4. Operator Overloading
- This program defines a class **ComplexAddition** to represent and add complex numbers.  
- The class has:
  - Data members: `real` (real part) and `imag` (imaginary part).  
  - A **constructor** to initialize complex numbers.  
  - A member function `add(int A, int B)` to display the result of addition.  
- In `main()`, two complex numbers are created, added together manually (real + real, imag + imag), and the result is displayed.  

---

##  Algorithm
1. **Start** the program.  
2. Define class `ComplexAddition` with:
   - Two integer data members: `real`, `imag`.  
   - A constructor to initialize and print the complex number.  
   - A member function `add(int A, int B)` to display the sum of two complex numbers.  
3. In `main()`:
   - Create object `A1(3, 2)` → represents `3 + 2i`.  
   - Create object `A2(8, 5)` → represents `8 + 5i`.  
   - Add real parts: `3 + 8 = 11`.  
   - Add imaginary parts: `2 + 5 = 7`.  
   - Call `A1.add(11, 7)` to display the result.  
4. **End** the program.  

---

##  5.Operator Overloading Example - Equality Operator (==)
- This program demonstrates **operator overloading** in C++.  
- A class `Number` is defined with:
  - A private data member `value`.  
  - A constructor to initialize the value.  
  - An overloaded `==` operator to compare two `Number` objects.  
- In `main()`, three objects are created and compared using the `==` operator.  
- The overloaded operator allows direct use of `n1 == n2` instead of writing a separate comparison function.  

---

##  Algorithm
1. **Start** the program.  
2. Define a class `Number` with:
   - A private integer `value`.  
   - A constructor to initialize the value.  
   - An overloaded operator function `operator==` that:
     - Takes another `Number` object as a parameter.  
     - Returns `true` if both objects have the same value, otherwise returns `false`.  
3. In `main()`:
   - Create objects `n1(10)`, `n2(10)`, `n3(20)`.  
   - Compare `n1` and `n2` using `==`.  
   - Compare `n1` and `n3` using `==`.  
   - Print whether they are equal or not.  
4. **End** the program.  

---

##  Conclusion
- Constructor overloading is a powerful feature in C++ that provides **flexibility in object creation**.  
- It allows initializing objects in **multiple ways** depending on the data available.  
- By defining multiple constructors, a class becomes **easier to use and more versatile**.  
- This concept follows **compile-time polymorphism**, as the constructor is chosen at compile time based on arguments.  
