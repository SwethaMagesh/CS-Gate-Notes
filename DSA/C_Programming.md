## Dynamic Allocation

## malloc()

- Garbage values initialised
- Single argument

## calloc()

- Initialised with 0
- 2 arguments. Eg: `calloc(10,sizeof(int))`

## realloc()

- Increase the existing size

## free()

- Deallocates Dynamically allocated values.

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

---
### typedef
- `typdef int char ;` is not valid
- 
