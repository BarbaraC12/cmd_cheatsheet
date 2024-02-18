# C++ Cheatsheet

## Table of Contents
1. [Basic Syntax](#basic-syntax)
2. [Data Types](#data-types)
3. [Control Structures](#control-structures)
4. [Functions](#functions)
5. [Arrays and Strings](#arrays-and-strings)
6. [Pointers](#pointers)
7. [Classes and Objects](#classes-and-objects)
8. [File Handling](#file-handling)
9. [Memory Management](#memory-management)
10. [Standard Template Library (STL)](#stl)

---

### Basic Syntax <a name="basic-syntax"></a>

#### Hello World
```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello, World!" << endl;
    return 0;
}
```

#### Comments
```cpp
// This is a single-line comment

/* 
   This is a multi-line comment
*/

```

#### Variables
```cpp
int age = 25;
double pi = 3.14;
char grade = 'A';
bool isStudent = true;
```

### Data Types <a name="data-types"></a>

#### Fundamental Data Types
- `int`
- `float`
- `double`
- `char`
- `bool`

#### Modifiers
- `short`
- `long`
- `unsigned`

#### Constants
```cpp
const int MAX_VALUE = 100;
```

### Control Structures <a name="control-structures"></a>

#### If-Else Statement
```cpp
if (condition) {
    // code if condition is true
} else {
    // code if condition is false
}
```

#### Switch Statement
```cpp
switch (variable) {
    case value1:
        // code for value1
        break;
    case value2:
        // code for value2
        break;
    default:
        // code if variable doesn't match any case
}
```

#### Loops
##### For Loop
```cpp
for (int i = 0; i < 5; i++) {
    // code to be executed
}
```

##### While Loop
```cpp
while (condition) {
    // code to be executed
}
```

##### Do-While Loop
```cpp
do {
    // code to be executed
} while (condition);
```

### Functions <a name="functions"></a>

#### Function Declaration
```cpp
// Function declaration
int add(int a, int b);

// Function definition
int add(int a, int b) {
    return a + b;
}

// Function call
int result = add(5, 3);
```

### Arrays and Strings <a name="arrays-and-strings"></a>

#### Arrays
```cpp
int numbers[] = {1, 2, 3, 4, 5};
cout << numbers[2]; // Output: 3
```

#### Strings
```cpp
#include <string>
using namespace std;

string greeting = "Hello, World!";
cout << greeting;
```

### Pointers <a name="pointers"></a>

#### Pointer Declaration and Initialization
```cpp
int num = 10;
int* ptr = &num;
```

#### Pointer Arithmetic
```cpp
int arr[] = {1, 2, 3};
int* ptr = arr;

cout << *ptr;   // Output: 1
cout << *(ptr+1); // Output: 2
```

### Classes and Objects <a name="classes-and-objects"></a>

#### Class Declaration
```cpp
class Car {
public:
    string brand;
    string model;
    int year;

    void displayInfo() {
        cout << "Brand: " << brand << ", Model: " << model << ", Year: " << year << endl;
    }
};
```

#### Object Creation and Usage
```cpp
Car myCar;
myCar.brand = "Toyota";
myCar.model = "Camry";
myCar.year = 2022;

myCar.displayInfo();
```

#### Inheritance
```cpp
class ElectricCar : public Car {
public:
    int batteryCapacity;
};

ElectricCar myElectricCar;
myElectricCar.brand = "Tesla";
myElectricCar.model = "Model S";
myElectricCar.year = 2023;
myElectricCar.batteryCapacity = 75;

myElectricCar.displayInfo();
cout << "Battery Capacity: " << myElectricCar.batteryCapacity << " kWh" << endl;
```

### File Handling <a name="file-handling"></a>

#### Reading from a File
```cpp
#include <fstream>
using namespace std;

ifstream inputFile("example.txt");
string line;

while (getline(inputFile, line)) {
    cout << line << endl;
}

inputFile.close();
```

#### Writing to a File
```cpp
#include <fstream>
using namespace std;

ofstream outputFile("output.txt");

outputFile << "This is a line in the file." << endl;

outputFile.close();
```

### Memory Management <a name="memory-management"></a>

#### Dynamic Memory Allocation
```cpp
int* numPtr = new int;
*numPtr = 5;
delete numPtr;
```

#### Arrays and Memory Allocation
```cpp
int* arrPtr = new int[5];
delete[] arrPtr;
```

### Standard Template Library (STL) <a name="stl"></a>

#### Vectors
```cpp
#include <vector>
using namespace std;

vector<int> numbers = {1, 2, 3, 4, 5};
numbers.push_back(6);
```

#### Maps
```cpp
#include <map>
using namespace std;

map<string, int> ages;
ages["Alice"] = 25;
ages["Bob"] = 30;
```

#### Iterators
```cpp
vector<int>::iterator it;

for (it = numbers.begin(); it != numbers.end(); ++it) {
    cout << *it << " ";
}
```
