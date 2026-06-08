# Python Exception Handling Across Function Calls

## 📌 Overview

This project demonstrates how exceptions raised inside a function can be handled by the calling code. The program accepts two integer inputs, performs integer division through a separate function, and handles exceptions in the main program using `try-except` blocks.

This example illustrates the concept of **exception propagation**, where errors occurring inside a function are passed back to the caller for handling.

---

## 🚀 Features

* Accepts user input for two integers
* Performs integer division using a separate function
* Demonstrates exception propagation
* Handles invalid input (`ValueError`)
* Handles division by zero (`ZeroDivisionError`)
* Clean and modular code structure

---

## 🛠️ Technologies Used

* Python 3

---

## 📂 Project Structure

```text
├── exception_propagation.py
├── README.md
```

---

## 💻 Source Code

```python
def division(x, y):
    d = x // y  # Integer division like Java
    print("Division is", d)


print("Program starts...")

try:
    a = int(input("Enter first number : "))
    b = int(input("Enter second number : "))

    division(a, b)

except ValueError:
    print("Error in data : Number not provided correctly")

except ZeroDivisionError:
    print("Error in data : Divisor should not be zero")

print("Program ends...")
```

---

## ▶️ How to Run

### Clone the Repository

```bash
git clone https://github.com/your-username/python-exception-propagation.git
cd python-exception-propagation
```

### Run the Program

```bash
python exception_propagation.py
```

---

## 📋 Sample Outputs

### Successful Execution

```text
Program starts...
Enter first number : 30
Enter second number : 5
Division is 6
Program ends...
```

### Division by Zero

```text
Program starts...
Enter first number : 30
Enter second number : 0
Error in data : Divisor should not be zero
Program ends...
```

### Invalid Input

```text
Program starts...
Enter first number : abc
Error in data : Number not provided correctly
Program ends...
```

---

## 🧠 Concepts Covered

* Functions in Python
* Exception Handling
* Exception Propagation
* `try-except` Blocks
* `ValueError`
* `ZeroDivisionError`
* Integer Division (`//`)

---

## 🔍 Exception Propagation

The `division()` function does not handle exceptions internally:

```python
def division(x, y):
    d = x // y
```

If an error occurs:

* `ZeroDivisionError` is raised inside the function.
* The exception propagates back to the caller.
* The `try-except` block in the main program catches and handles it.

This is a common practice in larger applications where lower-level functions allow higher-level code to decide how errors should be handled.

---

## 🎯 Learning Objectives

By studying this project, you will learn:

* How exceptions move through function calls
* When to handle exceptions inside a function vs outside
* How to build more maintainable Python programs
* The importance of centralized error handling

---

## 🔮 Future Improvements

* Support floating-point division
* Add custom exception messages
* Implement logging for errors
* Create a menu-driven calculator
* Add multiple mathematical operations

---

## 👨‍💻 Author

**Pranay Jadhao**

Electronics & Telecommunication Engineer

Aspiring Software & Embedded Systems Engineer

---

## 📄 License

This project is open-source and available for educational and learning purposes.

<img width="768" height="778" alt="image" src="https://github.com/user-attachments/assets/d4980a97-8359-4fc4-9ba5-a07d6e9669d0" />

Error when number is not provided correctly

<img width="503" height="239" alt="image" src="https://github.com/user-attachments/assets/cbecd58a-427b-48e1-92d7-88ec5f00fa5a" />
