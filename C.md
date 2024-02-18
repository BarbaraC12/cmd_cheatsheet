# C Programming Cheatsheet

## Basics

### Hello World
```c
#include <stdio.h>

int main() {
    printf("Hello, World!\n");
    return 0;
}
```

### Variables and Data Types
```c
int num = 10;
float floatNum = 3.14;
char letter = 'A';
```

### Input/Output
```c
scanf("%d", &num);
printf("The value is: %d\n", num);
```

## Control Structures

### Conditional Statements
```c
if (condition) {
    // code
} else if (another_condition) {
    // code
} else {
    // code
}
```

### Ternar Operator
```c
int result = (condition) ? value_if_true : value_if_false;
```

### Loops
```c
for (int i = 0; i < 5; i++) {
    // code
}

while (condition) {
    // code
}

do {
    // code
} while (condition);
```

## Functions

### Declaration
```c
int add(int a, int b);
```

### Definition
```c
int add(int a, int b) {
    return a + b;
}
```

### Call
```c
int result = add(3, 5);
```

## Arrays and Strings

### Arrays
```c
int numbers[5] = {1, 2, 3, 4, 5};
```

### Strings
```c
char greeting[] = "Hello, C!";
```

## Pointers

### Declaration
```c
int *ptr;
```

### Initialization
```c
int num = 10;
int *ptr = &num;
```

### Dereferencing
```c
int value = *ptr;
```

## Memory Management

### Dynamic Memory Allocation
```c
int *dynamicArray = (int*)malloc(5 * sizeof(int));
```

### Freeing Memory
```c
free(dynamicArray);
```

### Memory, Stack, and Variable Sizes

- **Memory**: The computer's memory is divided into two main parts - stack and heap.

- **Stack**: Used for function calls and local variables. It's a Last-In-First-Out (LIFO) data structure.

- **Heap**: Used for dynamic memory allocation. It's managed manually using functions like `malloc` and `free`.

- **Variable Sizes**:
  - `char`: 1 byte
  - `int`: 4 bytes
  - `float`: 4 bytes
  - `double`: 8 bytes

## File Handling

### Opening a File
```c
FILE *file = fopen("example.txt", "r");
```

### Reading from a File
```c
char buffer[100];
fscanf(file, "%s", buffer);
```

### Closing a File
```c
fclose(file);
```

## Miscellaneous

### Structures
```c
struct Point {
    int x;
    int y;
};
```

### Enumerations
```c
enum Day {SUNDAY, MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY};
```

### Regex
```c
#include <regex.h>

regex_t regex;
regcomp(&regex, "pattern", 0);
```

### Preprocessor Directives
```c
#define PI 3.14
```
