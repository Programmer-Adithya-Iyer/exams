C

---

# 📘 UNIT I – Programming in C (Expanded Notes)

---

## 1. Introduction to Programming

### Computer System & Components
- **Basic Operations:**
  - **Inputting:** Entering data/instructions via input devices (keyboard, mouse, scanner).
  - **Storing:** Saving data/results in memory (primary or secondary).
  - **Processing:** Arithmetic/logical operations performed by CPU.
  - **Outputting:** Displaying results in human-readable form (monitor, printer).
  - **Controlling:** CU directs sequence of operations.
- **Units:**
  - **Input Unit:** Converts human-readable input → machine-readable.
  - **Storage Unit:**
    - **Primary Storage (RAM):** Volatile, fast, limited.
    - **Secondary Storage (Disk):** Non-volatile, large, permanent.
  - **CPU:**
    - **ALU:** Executes arithmetic/logical ops.
    - **CU:** Controls flow of data/instructions.
  - **Output Unit:** Converts machine output → human-readable.

---

### Computing Environments
- **Personal Computing:** Standalone systems (PCs, laptops).
- **Time-Sharing:** Multiple users share CPU time slices.
- **Client-Server:** Client requests, server responds.
- **Distributed Computing:** Multiple nodes connected, working on one task.
- **Grid Computing:** Cluster of computers across locations solving one problem.
- **Cloud Computing:** On-demand resources (SaaS, PaaS, IaaS).
- **Cluster Computing:** Group of computers working as one system.

---

### Computer Languages
- **Machine Language:** Binary (0s, 1s), machine-dependent.
- **Assembly Language:** Mnemonics, machine-dependent.
- **High-Level Languages:** Human-readable, machine-independent (C, C++, Java).
- **Middle-Level Languages:** Assembly language (symbols + hardware awareness).

---

### Creating & Running Programs
1. **Write Source Code** (`.c` file).
2. **Compile:** Translates to object code.
3. **Link:** Combines object code + libraries.
4. **Execute:** Produces output.

---

### Preprocessor
- Handles directives before compilation.
- Examples:
  - `#include <stdio.h>` → Includes header file.
  - `#define PI 3.14` → Macro definition.

---

### Compilation Process
- **Steps:**
  1. Preprocessor → expanded code.
  2. Compiler → assembly code.
  3. Assembler → object code.
  4. Linker → executable file.
- **Role of Linker:** Combines object files + libraries into final executable.

---

### Invocation & Execution
- Program execution starts from `main()` function.
- Flow: Source → Compiler → Object → Linker → Executable → Run.

---

## 2. Algorithms

- **Algorithm:** Step-by-step instructions to solve a problem.
  - Must define input/output clearly.
  - Language-independent (general English).
- **Flowchart:** Graphical representation using symbols (oval = start/end, parallelogram = I/O, rectangle = process, diamond = decision).
- **Pseudocode:** Informal description of program logic, close to natural language.

---

## 3. Introduction to C Language

### History
- Developed at **Bell Labs (1972)** by **Dennis Ritchie**.
- Derived from **B** and **BCPL**.
- Used to implement **UNIX OS**.
- **Milestones:**
  - 1978: K&R C.
  - 1989: ANSI C.
  - 1999: C99.

---

### Why C is Popular
- Reliable, simple, portable.
- Small size (32 keywords).
- Structured, supports functions.
- Efficient, flexible (system + application programming).
- Supports pointers, bitwise operations.

---

### Structure of a C Program
1. Documentation (comments).
2. Preprocessor statements (`#include`).
3. Global declarations.
4. `main()` function:
   - Local declarations.
   - Program statements.
   - Function calls.
5. User-defined functions.

---

### Compilation & Execution of C Program
- Source file (`.c`) → Preprocessor → Compiler → Assembler → Object file (`.o`) → Linker → Executable (`.exe`).

---

## 4. C Tokens

- **Definition:** Smallest individual units in a C program.
- **Types:**
  1. **Keywords:** Reserved words (32 keywords: `int`, `char`, `if`, `else`, `return`, etc.).
  2. **Identifiers:** User-defined names (rules: start with letter/underscore, case-sensitive, max 31 chars).
  3. **Constants:**
     - Integer (e.g., 426, -8000).
     - Real (fractional/exponential form).
     - Character (e.g., `'A'`, `'6'`).
  4. **Strings:** Sequence of characters in double quotes (`"Hello"`).
  5. **Special Symbols:** `{}`, `()`, `[]`, `;`, `#`, etc.
  6. **Operators:** Arithmetic, relational, logical, etc.

---

## 5. Variables & Data Types

- **Variable:** Named storage location.  
  - Syntax: `datatype variable_name;`
- **Initialization:** Assign initial value (`int x=10;`).
- **Data Types:**
  - **Basic:** `int`, `char`, `float`, `double`.
  - **Qualifiers:** `short`, `long`, `signed`, `unsigned`.
  - **Ranges:**
    - `char`: -128 to 127.
    - `unsigned char`: 0 to 255.
    - `int`: -32,768 to 32,767 (2 bytes).
    - `float`: 6 decimal precision.
    - `double`: 15 decimal precision.

---

## 6. I/O Statements
- **`printf`:** Output formatted data.
- **`scanf`:** Input formatted data.
- Defined in `stdio.h`.

---

## 7. Interconversion of Variables
- **Implicit Conversion (Type Promotion):** Automatic widening (e.g., `int` → `float`).
- **Explicit Conversion (Type Casting):** Programmer-defined using `(datatype)` operator.  
  Example:  
  ```c
  double x = 1.2;
  int sum = (int)x + 1; // sum = 2
  ```

---

## 8. Operators & Expressions

### Types of Operators
1. **Arithmetic:** `+`, `-`, `*`, `/`, `%`
2. **Relational:** `<`, `>`, `<=`, `>=`, `==`, `!=`
3. **Logical:** `&&`, `||`, `!`
4. **Assignment:** `=`, `+=`, `-=`, `*=`, `/=`
5. **Increment/Decrement:** `++`, `--`
6. **Bitwise:** `&`, `|`, `^`, `~`, `<<`, `>>`
7. **Conditional (Ternary):** `?:`
8. **Special Operators:**
   - `sizeof` → size of datatype.
   - `,` (comma operator).
   - `->` (structure pointer access).

---

### Operator Precedence & Associativity
- **Highest:** `()` (function call), `[]` (array).
- **Unary:** `++`, `--`, `!`, `sizeof` (Right-to-Left).
- **Multiplication/Division/Modulo:** Left-to-Right.
- **Addition/Subtraction:** Left-to-Right.
- **Relational/Equality:** Left-to-Right.
- **Logical AND/OR:** Left-to-Right.
- **Conditional `?:`:** Right-to-Left.
- **Assignment:** Right-to-Left.
- **Lowest:** Comma `,` (Left-to-Right).

---

### Evaluation of Expressions
- Expressions are evaluated based on precedence and associativity.
- Example:
  ```c
  int x=10, y=5;
  int exp = y * (x / y + x / y); // precedence of / before +
  ```

---

### Type Conversions in Expressions
- **Implicit:** Automatic promotion (e.g., `char` → `int`).
- **Explicit (Casting):** Programmer forces conversion using `(type)`.

---

# 📌 Must-Remember Terms & Key Points (Cheat Sheet)

- **Computer System:** Input, Storage, CPU (ALU+CU), Output, Control.  
- **Environments:** Personal, Time-sharing, Client-server, Distributed, Grid, Cloud, Cluster.  
- **Languages:** Machine (binary), Assembly (mnemonics), High-level (C, Java), Middle-level.  
- **Program Execution:** Source → Compiler → Linker → Executable.  
- **Algorithm Tools:** Flowchart (symbols), Pseudocode (English-like).  
- **C History:** Dennis Ritchie, 1972, UNIX, ANSI C (1989).  
- **C Program Structure:** Documentation → Preprocessor → Declarations → `main()` → Functions.  
- **Tokens:** Keywords (32), Identifiers, Constants, Strings, Special symbols, Operators.  
- **Variables/Data Types:** int, char, float, double, signed/unsigned, short/long.  
- **I/O



---

# 📘 UNIT II – Programming in C (Master Notes)

---

## 1. Control Structures

### Introduction
- Control structures determine the **flow of execution** in a program.
- Types:
  1. **Decision Statements (Selection/Branching)**
  2. **Loop Control Statements (Iteration)**
  3. **Jump Statements**

---

### A. Decision Statements

#### `if` Statement
- **Syntax:**
  ```c
  if (condition) {
      statements;
  }
  ```
- Executes block only if condition is true (non-zero).
- Example:
  ```c
  if (x > 0) printf("Positive");
  ```

#### `if-else` Statement
- Two-way branching.
- **Syntax:**
  ```c
  if (condition) {
      // true block
  } else {
      // false block
  }
  ```

#### Nested `if-else`
- One `if-else` inside another.
- Example: Checking relation between two numbers.

#### `else-if` Ladder
- Multi-way branching.
- **Syntax:**
  ```c
  if (cond1) { ... }
  else if (cond2) { ... }
  else { ... }
  ```

#### `switch` Statement
- Multi-way branching based on integer/char expression.
- **Syntax:**
  ```c
  switch(expression) {
      case const1: statements; break;
      case const2: statements; break;
      ...
      default: statements;
  }
  ```
- **Important:** Use `break` to prevent fall-through.
- Example: Grade evaluation.

---

### B. Loop Control Statements

#### `while` Loop
- Entry-controlled loop.
- Executes block repeatedly while condition is true.
- **Syntax:**
  ```c
  while(condition) {
      statements;
  }
  ```

#### `do-while` Loop
- Exit-controlled loop.
- Executes block at least once.
- **Syntax:**
  ```c
  do {
      statements;
  } while(condition);
  ```

#### `for` Loop
- Compact loop with init, condition, update in one line.
- **Syntax:**
  ```c
  for(init; condition; update) {
      statements;
  }
  ```

#### Nesting of Loops
- One loop inside another.
- Any type of loop can be nested.

---

### C. Jump Statements

#### `break`
- Exits innermost loop or `switch` immediately.

#### `continue`
- Skips rest of loop body, goes to next iteration.

#### `goto`
- Jumps to labeled statement.
- **Syntax:**
  ```c
  goto label;
  ...
  label: statements;
  ```
- **Note:** Considered harmful, use sparingly.

---

## 2. Arrays

### Concepts
- **Definition:** Collection of elements of same type stored in contiguous memory.
- **Indexing:** Starts from 0.
- **Advantages:** Easy access, efficient storage, sequential processing.

---

### One-Dimensional Arrays
- **Declaration:**
  ```c
  int arr[10];
  ```
- **Initialization:**
  ```c
  int arr[5] = {1, 2, 3, 4, 5};
  ```
- **Accessing:**
  ```c
  printf("%d", arr[2]); // prints 3
  ```

---

### Two-Dimensional Arrays
- **Declaration:**
  ```c
  int matrix[3][3];
  ```
- **Initialization:**
  ```c
  int matrix[2][2] = {{1,2}, {3,4}};
  ```
- **Accessing:**
  ```c
  printf("%d", matrix[1][0]); // prints 3
  ```

---

### Multi-Dimensional Arrays
- Arrays with more than two dimensions (rare in practice).
- Example: `int cube[3][3][3];`

---

## 3. Functions

### User-Defined Functions
- **Parts:** Declaration (prototype), Definition, Call.
- **Advantages:** Modular, reusable, easier debugging.

### Built-in Functions
- Provided by C standard library (e.g., `printf`, `scanf`, `strlen`).

---

### Storage Classes
- **auto:** Default, local scope.
- **static:** Retains value between calls.
- **extern:** Refers to global variable defined elsewhere.
- **register:** Requests storage in CPU register (faster access).

---

### Parameter Passing
- **Call by Value:** Copy of actual argument passed. Changes don’t affect original.
- **Call by Reference (via arrays/pointers):** Address passed. Changes affect original.

---

### Passing Arrays to Functions
- Arrays are always passed by reference (address of first element).
- Example:
  ```c
  void display(int arr[], int n) {
      for(int i=0;i<n;i++) printf("%d ", arr[i]);
  }
  ```

---

### Recursion
- Function calling itself.
- Example: Factorial
  ```c
  int fact(int n) {
      if(n==0) return 1;
      else return n*fact(n-1);
  }
  ```

---

## 4. Strings

### Concepts
- **Definition:** Array of characters terminated by `'\0'`.
- **Declaration:**
  ```c
  char str[20];
  ```
- **Initialization:**
  ```c
  char str[] = "Hello";
  ```

---

### Variable Length Strings
- Strings can be shorter than declared size.
- Example: `char name[50];` can hold up to 49 chars + `'\0'`.

---

### Inputting Strings
- **Using `scanf`:**
  ```c
  scanf("%s", str); // stops at whitespace
  ```
- **Using `gets`:** Reads entire line (unsafe, deprecated).
- **Using `fgets`:** Safer alternative.

---

### String Library Functions (`string.h`)
- `strlen(str)` → length of string.
- `strcpy(dest, src)` → copy string.
- `strcat(str1, str2)` → concatenate.
- `strcmp(str1, str2)` → compare.
- `strchr(str, ch)` → find character.
- `strstr(str, substr)` → find substring.

---

### String Handling Examples
```c
char s1[20] = "Hello";
char s2[20] = "World";
printf("%d", strlen(s1)); // 5
strcat(s1, s2); // s1 = "HelloWorld"
```

---

# 📌 Must-Remember Terms & Key Points (Cheat Sheet)

### Control Structures
- **Decision:** if, if-else, else-if, switch.
- **Loops:** while (entry), do-while (exit), for (compact).
- **Jump:** break, continue, goto.

### Arrays
- **1D:** `int arr[10];`
- **2D:** `int matrix[3][3];`
- **Multi-D:** `int cube[3][3][3];`
- **Always contiguous memory.**

### Functions
- **User-defined vs Built-in.**
- **Storage classes:** auto, static, extern, register.
- **Parameter passing:** Call by value vs Call by reference.
- **Recursion:** Function calling itself.

### Strings
- **Character array terminated by `'\0'`.**
- **Input:** scanf, gets, fgets.
- **Library functions:** strlen, strcpy, strcat, strcmp, strchr, strstr.


---

# 📘 UNIT III – Programming in C (Master Notes)

---

## 1. Pointers

### Pointer Basics
- **Definition:** A pointer is a variable that stores the address of another variable.
- **Declaration:**
  ```c
  int *p;   // pointer to int
  char *c;  // pointer to char
  ```
- **Initialization:**
  ```c
  int x = 10;
  int *p = &x;   // p stores address of x
  ```
- **Dereferencing:** Accessing value at the address stored in pointer using `*`.
  ```c
  printf("%d", *p); // prints 10
  ```

### Address-of Operator (`&`)
- Returns address of a variable.
- Example:
  ```c
  int x=50;
  printf("%u", &x);
  ```

### NULL Pointer
- Pointer that points to nothing.
- Example: `int *p = NULL;`
- Used for safe initialization.

---

### Pointer Arithmetic
- Allowed operations: `++`, `--`, `+n`, `-n`, subtraction between pointers.
- Formula:  
  `new_address = current_address ± (n * size_of(data type))`
- Example:
  ```c
  int arr[5] = {1,2,3,4,5};
  int *p = arr;
  for(int i=0;i<5;i++) printf("%d ", *(p+i));
  ```

---

### Pointers to Pointers (Double Pointers)
- Pointer storing address of another pointer.
- Example:
  ```c
  int a=10;
  int *p=&a;
  int **pp=&p;
  printf("%d", **pp); // prints 10
  ```

---

### Generic Pointers (Void Pointers)
- Can store address of any data type.
- Must be typecast before dereferencing.
- Example:
  ```c
  void *ptr;
  int x=90;
  ptr=&x;
  printf("%d", *(int*)ptr);
  ```

---

### Array of Pointers
- Array whose elements are pointers.
- Example:
  ```c
  int a[3]={10,20,30};
  int *p[3]={&a[0],&a[1],&a[2]};
  printf("%d", *p[1]); // prints 20
  ```

---

### Functions Returning Pointers
- Example:
  ```c
  int* getArray() {
      static int arr[3]={1,2,3};
      return arr;
  }
  ```

---

### Dynamic Memory Allocation (`stdlib.h`)
- **malloc():** Allocates single block, uninitialized.
- **calloc():** Allocates multiple blocks, initialized to 0.
- **realloc():** Resizes previously allocated block.
- **free():** Deallocates memory.
- Example:
  ```c
  int *p = (int*)malloc(5*sizeof(int));
  free(p);
  ```

---

### Pointers to Functions
- Store address of a function.
- Example:
  ```c
  int add(int a,int b){return a+b;}
  int (*fp)(int,int)=&add;
  printf("%d", fp(2,3)); // prints 5
  ```

---

### Pointers and Strings
- Strings are arrays of characters; pointers can traverse them.
- Example:
  ```c
  char str[]="Hello";
  char *p=str;
  while(*p!='\0'){printf("%c",*p); p++;}
  ```

---

## 2. Structures and Unions

### Structure Definition
- User-defined data type grouping different types.
- Example:
  ```c
  struct Student {
      int roll;
      char name[20];
      float marks;
  };
  ```

### Initialization & Accessing
- Example:
  ```c
  struct Student s1={1,"Rahul",85.5};
  printf("%s", s1.name);
  ```

### Nested Structures
- Structures inside structures.
- Example:
  ```c
  struct Address {char city[20]; int pin;};
  struct Employee {char name[20]; struct Address addr;};
  ```

### Arrays of Structures
- Example:
  ```c
  struct Student s[3]={{1,"A",90},{2,"B",85},{3,"C",80}};
  ```

### Structures and Functions
- Passed by value or reference.
- Example:
  ```c
  void display(struct Student st){printf("%s",st.name);}
  ```

### Self-Referential Structures
- Structure containing pointer to same type.
- Example:
  ```c
  struct Node {int data; struct Node *next;};
  ```

---

### Union
- Similar to structure but members share same memory.
- Only one member active at a time.
- Example:
  ```c
  union Data {int i; char c;};
  ```

### Difference Between Structure and Union
| Feature | Structure | Union |
|---------|-----------|-------|
| Memory  | Allocates for all members | Allocates for largest member |
| Members | All can hold values simultaneously | Only one at a time |
| Size    | Sum of all members | Size of largest member |

---

### Typedef
- Provides alias name for data type.
- Example:
  ```c
  typedef unsigned int unit;
  unit x=10;
  ```

---

### Enumerations
- User-defined type for named integer constants.
- Example:
  ```c
  enum Weekday {Sun,Mon,Tue,Wed,Thu,Fri,Sat};
  ```

---

## 3. File Handling

### Command Line Arguments
- `main(int argc, char *argv[])`
- `argc` → number of arguments, `argv` → array of strings.

### File Modes
- `r` → read, `w` → write, `a` → append.
- `r+`, `w+`, `a+` → read/write.
- Binary modes: `rb`, `wb`, `ab`.

### Basic File Operations
- **fopen():** Open file.
- **fprintf():** Write formatted data.
- **fscanf():** Read formatted data.
- **fputc():** Write character.
- **fgetc():** Read character.
- **fclose():** Close file.
- **fseek():** Move file pointer.
- **ftell():** Current position.
- **rewind():** Reset pointer.

---

## 4. Scope and Life of Variables

### Scope
- **Local:** Declared inside function/block.
- **Global:** Declared outside all functions.
- **Formal Parameters:** Scope within function call.

### Lifetime
- **auto:** Default, destroyed when block ends.
- **static:** Retains value between calls.
- **register:** Stored in CPU register, fast access.
- **extern:** Refers to global variable defined elsewhere.

---

## 5. Multi-file Programming
- Large programs split into multiple source files.
- **Header files (.h):** Contain declarations.
- **Source files (.c):** Contain definitions.
- **Linker:** Combines object files into executable.
- **Advantages:** Modularity, reusability, easier debugging.

---

# 📌 Must-Remember Terms & Key Points (Cheat Sheet)

### Pointers
- Basics: `*` dereference, `&` address-of.
- Arithmetic: `p+1` moves to next element.
- Double pointers: `**pp`.
- Void pointers: Generic, typecast before use.
- Dynamic memory: malloc, calloc, realloc, free.
- Function pointers: `int (*fp)(int,int)`.

### Structures & Unions
- Structure: Different types grouped.
- Union: Shared memory, one active member.
- Typedef: Alias for data type.
- Enum: Named integer constants.
- Self-referential structures: Linked lists.

### File Handling
- Modes: r, w, a, rb, wb, ab.
- Functions: fopen, fclose, fprintf, fscanf, fgetc, fputc, fseek, ftell, rewind.
- Command line arguments: `argc`, `argv`.

### Scope & Lifetime
- auto, static, register, extern.
- Local vs Global variables.

### Multi-file Programming
- Header files (.h), source files (.c), linker.
- Promotes modularity and reusability.


---

# UNIT IV – Programming in C (Plain Text Notes)

---

## Preprocessor Directives

Preprocessor directives are instructions executed before compilation. They always begin with `#`.

- `#` : General preprocessor operator. Used in directives like `#include`, `#define`.
- `##` : Token pasting operator. Concatenates two tokens into one. Example: `#define merge(a,b) a##b` → `int number=100;`.
- `#define` : Defines macros (constants or function-like). Example: `#define PI 3.14159` or `#define SQUARE(x) (x*x)`.
- `#if` : Conditional compilation. Example:  
  ```
  #define VALUE 10
  #if VALUE > 5
  printf("Condition true");
  #endif
  ```
- `#ifdef` : Compiles block if macro is defined. Example:  
  ```
  #define DEBUG
  #ifdef DEBUG
  printf("Debug mode ON");
  #endif
  ```
- `#ifndef` : Compiles block if macro is not defined. Example:  
  ```
  #ifndef HEADER_FILE
  #define HEADER_FILE
  // code
  #endif
  ```
- `#if … #else` : Conditional compilation with alternative path. Example:  
  ```
  #define VALUE 3
  #if VALUE==3
  printf("Value is 3");
  #else
  printf("Value is not 3");
  #endif
  ```

---

## C Standard Libraries

- `stdio.h` : Input/Output functions like printf, scanf, fopen, fclose, gets, puts.
- `stdlib.h` : General utilities, memory management, conversions. Functions include malloc, calloc, free, atoi, rand, srand, system.
- `assert.h` : Debugging support. Function assert(expression).
- `math.h` : Mathematical operations. Functions include sqrt, pow, fabs, ceil, floor, sin, cos.
- `time.h` : Date and time functions. Functions include time, ctime, difftime, clock, localtime.
- `ctype.h` : Character classification and conversion. Functions include isalnum, isdigit, isalpha, toupper, tolower.
- `string.h` : String handling and manipulation. Functions include strlen, strcpy, strcat, strcmp, memcpy, memset.
- `stdarg.h` : Handling variable argument lists. Functions include va_start, va_arg, va_end, va_list.

---

## C99 Extensions

- New data types:  
  `_Bool` represents boolean values (0 false, 1 true).  
  `bool` from `<stdbool.h>` with true and false keywords.  
  `long long int` larger integer type.  
  `_Complex` and `_Imaginary` from `<complex.h>` for complex numbers.  
  Exact-width integers like int8_t, int16_t, int32_t, int64_t from `<stdint.h>`.  
  `float_t` and `double_t` from `<math.h>` for floating precision types.

- Inline functions: Use `inline` keyword for small functions to boost performance. Example: `inline int add(int a,int b){return a+b;}`.

- Single-line comments: `// comment` supported (like C++ style).

---

## Basic Algorithms

### Factorial
```
long long fact=1;
for(int i=1;i<=n;i++) fact*=i;
```
Time complexity O(n).

### Fibonacci Series
```
int a=0,b=1,c;
printf("%d %d ",a,b);
for(int i=3;i<=n;i++){c=a+b; printf("%d ",c); a=b; b=c;}
```
Time complexity O(n).

### Linear Search
Sequentially checks each element.
```
for(int i=0;i<n;i++) if(arr[i]==key) return i;
```
Time complexity O(n).

### Binary Search
Works on sorted array.
```
while(low<=high){
 mid=(low+high)/2;
 if(arr[mid]==key) return mid;
 else if(arr[mid]<key) low=mid+1;
 else high=mid-1;
}
```
Time complexity O(log n).

---

### Sorting Algorithms

#### Bubble Sort
Repeatedly swaps adjacent elements until sorted.  
Time complexity best O(n), worst O(n²).
```
for(i=0;i<n-1;i++)
 for(j=0;j<n-i-1;j++)
   if(arr[j]>arr[j+1]) swap(arr[j],arr[j+1]);
```

#### Selection Sort
Finds minimum element and places it at correct position.  
Time complexity O(n²).
```
for(i=0;i<n-1;i++){
 min=i;
 for(j=i+1;j<n;j++) if(arr[j]<arr[min]) min=j;
 swap(arr[min],arr[i]);
}
```

#### Insertion Sort
Inserts each element into its correct position in sorted part.  
Time complexity best O(n), worst O(n²).
```
for(i=1;i<n;i++){
 key=arr[i]; j=i-1;
 while(j>=0 && arr[j]>key){arr[j+1]=arr[j]; j--;}
 arr[j+1]=key;
}
```

---

### Square Root of a Number
Using sqrt() from math.h.
```
double res = sqrt(x);
```

---

### Array Order Reversal
```
for(i=0;i<n/2;i++){
 temp=arr[i];
 arr[i]=arr[n-1-i];
 arr[n-1-i]=temp;
}
```

---

### String Reversal
```
int len=strlen(str);
for(i=0;i<len/2;i++){
 char temp=str[i];
 str[i]=str[len-1-i];
 str[len-1-i]=temp;
}
```

---

## Must-Remember Points

- Preprocessor directives: #, ##, #define, #if, #ifdef, #ifndef, #else.  
- Libraries: stdio.h, stdlib.h, assert.h, math.h, time.h, ctype.h, string.h, stdarg.h.  
- C99 extensions: _Bool, bool, long long, _Complex, _Imaginary, exact-width integers, inline functions, // comments.  
- Algorithms: Factorial, Fibonacci, Linear search O(n), Binary search O(log n), Bubble sort O(n²), Selection sort O(n²), Insertion sort O(n²), Square root using sqrt(), Array reversal, String reversal.

---
