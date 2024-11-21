
### Round 1: Easy Level
1. **What is the correct syntax to declare a variable in C?**
   ```c
   int x;
   ```
2. **How do you comment a single line in C?**
   ```c
   // This is a single-line comment
   ```
3. **What does the `printf()` function do?**
   - It prints formatted output to the console.
4. **How do you declare a constant variable in C?**
   ```c
   const int x = 10;
   ```
5. **What will be the output of the following code?**
   ```c
   int x = 5;
   printf("%d", x);
   ```
   - Output: `5`
6. **What is the size of the `int` data type in C?**
   - Typically 4 bytes, but it can vary.
7. **How do you start a block of code in C?**
   ```c
   {
   ```
8. **What does the `return` statement do in a function?**
   - It exits the function and optionally returns a value.
9. **How do you declare an array of 5 integers in C?**
   ```c
   int arr[5];
   ```
10. **What is the value of `x` after the following code executes?**
    ```c
    int x = 10;
    x = x + 5;
    ```
    - Value: `15`
11. **What is the purpose of the `main()` function in a C program?**
    - It's the entry point of a C program.
12. **How do you declare a float variable in C?**
    ```c
    float y;
    ```
13. **What does `\n` signify in C?**
    - It represents a new line character.
14. **How do you declare a function that returns an integer?**
    ```c
    int function_name();
    ```
15. **What keyword is used to include a library in a C program?**
    ```c
    #include
    ```
16. **What will be the output of the following code?**
    ```c
    int a = 5, b = 10;
    printf("%d", a + b);
    ```
    - Output: `15`
17. **What is the use of `scanf()` function?**
    - It reads formatted input from the console.
18. **How do you declare a character variable in C?**
    ```c
    char ch;
    ```
19. **What is a pointer in C?**
    - It's a variable that stores the memory address of another variable.
20. **What is the purpose of a `#define` directive?**
    - It defines a macro.

### Round 2: Medium Level
1. **Explain the difference between `++i` and `i++`.**
   - `++i` increments the value of `i` and then returns it, while `i++` returns the value of `i` and then increments it.
2. **How do you create a function in C that returns an integer and takes two integer parameters?**
   ```c
   int function_name(int a, int b);
   ```
3. **What is the purpose of the `#include <stdio.h>` directive?**
   - It includes the standard input-output library functions.
4. **What will be the output of the following code snippet?**
   ```c
   int a = 10;
   int b = 20;
   int c = a + b;
   printf("%d", c);
   ```
   - Output: `30`
5. **How do you declare an array of 10 integers in C?**
   ```c
   int arr[10];
   ```
6. **What is a pointer and how is it declared in C?**
   - A pointer is a variable that stores the memory address of another variable. Declared as:
   ```c
   int *ptr;
   ```
7. **What is the difference between `while` and `do-while` loops?**
   - `while` loop checks the condition before executing the block, `do-while` loop checks the condition after executing the block.
8. **What is a `struct` in C?**
   - A `struct` is a user-defined data type that groups related variables of different types.
9. **How do you declare a multi-dimensional array in C?**
   ```c
   int arr[3][3];
   ```
10. **What is the use of the `sizeof` operator?**
    - It returns the size of a data type or variable.
11. **How do you swap two variables using pointers in C?**
    ```c
    void swap(int *a, int *b) {
        int temp = *a;
        *a = *b;
        *b = temp;
    }
    ```
12. **What is dynamic memory allocation in C?**
    - Allocating memory at runtime using functions like `malloc`, `calloc`, `realloc`, and `free`.
13. **What will be the output of the following code snippet?**
    ```c
    int x = 5;
    if (x > 0) {
        printf("Positive");
    } else {
        printf("Non-positive");
    }
    ```
    - Output: `Positive`
14. **How do you write a function that takes a string as an argument in C?**
    ```c
    void function_name(char str[]);
    ```
15. **What is the difference between `break` and `continue` statements?**
    - `break` exits a loop, while `continue` skips to the next iteration.
16. **How do you check for a null pointer in C?**
    ```c
    if (ptr == NULL) {
        // pointer is null
    }
    ```
17. **What is a union in C and how is it different from a struct?**
    - A union is a user-defined data type where all members share the same memory location. It is different from a struct where each member has its own memory location.
18. **Explain the concept of recursion in C.**
    - Recursion is a function calling itself to solve a smaller instance of the problem.
19. **What will be the output of the following code?**
    ```c
    int a = 5;
    printf("%d", a++);
    ```
    - Output: `5`
20. **How do you use the `switch` statement in C?**
    ```c
    switch (expression) {
        case value1:
            // statements
            break;
        case value2:
            // statements
            break;
        default:
            // default statements
    }
    ```

### Round 3: Hard Level
1. **Describe what pointers are and how they are used in C.**
   - Pointers are variables that store memory addresses. They are used for dynamic memory allocation, arrays, and functions.
2. **Write a C program to reverse a string using a pointer.**
    ```c
    #include <stdio.h>
    void reverse(char *str) {
        char *end = str;
        char temp;
        if (str) {
            while (*end) {
                ++end;
            }
            --end;
            while (str < end) {
                temp = *str;
                *str++ = *end;
                *end-- = temp;
            }
        }
    }
    int main() {
        char str[] = "Hello";
        reverse(str);
        printf("%s", str);
        return 0;
    }
    ```
3. **Explain the difference between `malloc` and `calloc` functions.**
   - `malloc` allocates uninitialized memory, whereas `calloc` allocates zero-initialized memory.
4. **What is a `struct` and how is it used in C?**
   - A `struct` is a user-defined data type that groups variables of different types under a single name.
    ```c
    struct Student {
        char name[50];
        int age;
        float marks;
    };
    ```
5. **Given the following code, what will be the output and why?**
    ```c
    void func(int *ptr)
    {
        *ptr = 10;
    }
    int main()
    {
        int x = 5;
        func(&x);
        printf("%d", x);
        return 0;
    }
    ```
    - Output: `10`. The function changes the value of `x` through the pointer.
6. **How do you declare and initialize a pointer to an integer in C?**
    ```c
    int a = 10;
    int *ptr = &a;
    ```
7. **What is the purpose of the `volatile` keyword in C?**
   - It tells the compiler that a variable's value may be changed by something outside the control of the code.
8. **How do you pass a pointer to a function in C?**
    ```c
    void function(int *ptr) {
        // function body
    }
    ```
9. **Explain the concept of dynamic memory allocation in C.**
   - Dynamic memory allocation allows programs to allocate memory during runtime using `malloc`, `calloc`, `realloc`, and `free` functions.
10. **What is the difference between `malloc` and `calloc` functions in C?**
    - `malloc` allocates a single block of memory while `calloc` allocates multiple blocks of memory and initializes them