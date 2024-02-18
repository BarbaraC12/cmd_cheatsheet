# Python Basics Cheatsheet

## Variables and Data Types

```python
# Variable assignment
x = 5
name = "Alice"
is_student = True

# Data types
# Integer
age = 25
# Float
height = 1.75
# String
message = "Hello, World!"
# Boolean
is_raining = False
```

## Basic Operations

```python
# Arithmetic operations
result = 10 + 5
difference = 20 - 8
product = 4 * 3
quotient = 15 / 5
remainder = 17 % 4

# Exponential
power = 2 ** 3

# Concatenation
greeting = "Hello" + " " + "World"
```

## Control Structures

### Conditional Statements

```python
# If statement
x = 10
if x > 5:
    print("x is greater than 5")
elif x == 5:
    print("x is equal to 5")
else:
    print("x is less than 5")

# Ternary operator
is_adult = True
status = "Adult" if is_adult else "Minor"
```

### Loops

```python
# While loop
count = 0
while count < 5:
    print(count)
    count += 1

# For loop
for i in range(5):
    print(i)
```

## Data Structures

### Lists

```python
# List creation
numbers = [1, 2, 3, 4, 5]
fruits = ["apple", "banana", "orange"]

# Accessing elements
first_number = numbers[0]
last_fruit = fruits[-1]

# Slicing
sliced_numbers = numbers[1:3]  # [2, 3]
```

### Dictionaries

```python
# Dictionary creation
person = {"name": "Alice", "age": 30, "city": "New York"}

# Accessing values
person_name = person["name"]
person_age = person.get("age")

# Adding or updating values
person["email"] = "alice@example.com"

# Looping through keys and values
for key, value in person.items():
    print(key, ":", value)
```

### Tuples

```python
# Tuple creation
coordinates = (10, 20)

# Accessing elements
x_coord = coordinates[0]
y_coord = coordinates[1]

# Unpacking
x, y = coordinates
```

### Sets

```python
# Set creation
unique_numbers = {1, 2, 3, 4, 5}

# Adding elements
unique_numbers.add(6)

# Removing elements
unique_numbers.remove(5)

# Set operations
set1 = {1, 2, 3}
set2 = {3, 4, 5}
union = set1 | set2
intersection = set1 & set2
difference = set1 - set2
```

## Functions

```python
# Function definition
def greet(name):
    return "Hello, " + name + "!"

# Function call
greeting = greet("Alice")
```

## Terminal Commands

### Package Management

```bash
# Install a package using pip
pip install package_name

# Uninstall a package using pip
pip uninstall package_name

# List installed packages
pip list
```

### Virtual Environments

```bash
# Create a virtual environment
python -m venv venv_name

# Activate virtual environment (Linux/Mac)
source venv_name/bin/activate

# Activate virtual environment (Windows)
venv_name\Scripts\activate
```
