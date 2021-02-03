- C and C++ are context-sensitive languages.
## Pointer
- `int *A [10], B[10][10];  `
- Of the following expressions
1. A[2]
1.  A[2][3]
1.  **B[1] - invalid**
1.  B[2][3]
- Remaining are valid LHS for assignment statements

## Dynamic Allocation


## malloc()

- Garbage values initialised
- Single argument
- 
```
int *g (void)  
{  
  int *px;  
  px = (int *) malloc (sizeof(int));  
  *px = 10; 
  return px;  
}  
```
- Causes no problem. The allocated memory on heap and can be used anytime


## calloc()

- Initialised with 0
- 2 arguments. Eg: `calloc(10,sizeof(int))`

## realloc()

- Increase the existing size
- Eg: ` ptr_new = (int *)realloc(ptr, sizeof(int)*3);`

## free()

- Deallocates Dynamically allocated values.

## Array
- Row major order address calculation: 
`Address of A [ I ][ J ] = B + W * [ N * ( I – Lr ) + ( J – Lc ) ]`
- *Where,
B = Base address
I = Row subscript of element whose address is to be found
J = Column subscript of element whose address is to be found
W = Storage Size of one element stored in the array (in byte)
Lr = Lower limit of row/start row index of matrix, if not given assume 0 (zero)
Lc = Lower limit of column/start column index of matrix, if not given assume 0 (zero)
M = Number of row of the given matrix
N = Number of column of the given matrix*

---
## User-Defined Types

- Classes
- Enumerations
- typedef definitions
- Structures (or records)

## Struct

- Structures in C cannot have member functions(also constructors) inside structure but Structures in C++ can have member functions along with data members.
- We cannot directly initialize structure data members in C but we can do it in C++.

  - ```
        struct testing
         {
             int x=7;
        };
     ```
  - This is valid in C++ and invalid in C
- C structures cannot have static members but is allowed in C++.
- sizeof operator: This operator will generate 0 for an empty structure in C whereas 1 for an empty structure in C++.
- Access specifiers (private, public, protected) are allowed in C++ and not in C
- Diff between class and struct:
  - class members are by default private
  - struct members are by default public

---

## Union

- Size of a union is taken according the size of largest member in union.
- Base address is same as base address of each member

 ![image](https://user-images.githubusercontent.com/43994542/104040792-1c1ae600-51fe-11eb-8182-692b34ea0f78.PNG)

---
### typedef
- `typdef int char ;` is not valid
---
## Points to Remember
###  Switch case statement 
1. Expression must be int, char or enum
1. Continuous execution till break
1. Default can be placed anywhere
1. Statements above first case, never executed
1. Case labels can not have variable names. (only constant allowed)
1. Case labels can not have same value
