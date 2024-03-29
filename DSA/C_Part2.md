### Some points to remember
- Pointers contain addresses. Adding, Subtracting, Dividing two addresses makes no sense because there is no idea what it would point to. Only Subtraction (To calculate the offset), Increment, Decrement, Adding integer, Subtracting integer is allowed. 
- The maximum number of arguments that can be passed in a single function are **253**
- Floating point numbers can have e,E
- Switch can have default case in between also
- volatile keyword - Compiler cannot optimise
- swap using ` a=a-b; b=a+b; a=b-a; ` May not work for all inputs as arithmetic overflow can occur.
- Important advice: ***Trace static and others with caution*** 
- #### Activation record (new concept)
- An activation record is another name for Stack Frame.
- It's the data structure that composes a call stack. It is generally composed of:
    - Locals to the callee
    - Return address to the caller
    - Parameters of the callee
    - The previous stack pointer (SP) value
- [For more details](https://stackoverflow.com/questions/1266233/what-is-activation-record-in-the-context-of-c-and-c)
- #### Storage classes
1. Auto
    - stored in stack
    - init to garbage value
    - can be accessed outside scope by using pointer which has its address.
1. Static
    - stored in data segment
    - Value retained even after the function is out of scope
    - init to 0
    - Can be local or global
    - Global static can be accessed anywhere
1. Register
    - stored in register for faster access
    - init to garbage value
    - if free register not available, will be stored in memory only
    - Pointers can't be used to get its address
1. Extern
    - stored in data segment
    - declared in another file
    - init to 0
- Difference between constant pointer and a pointer to a constant. 
    - `int * const ptr —> ptr` is constant pointer. You can change the value at the location pointed by pointer p, but you can not change p to point to other location.
    - ` int const * ptr —> ptr `is a pointer to a constant. You can change ptr to point other variable. But you cannot change the value pointed by ptr.
        - but if `x =4 ; int const *i=&p; x=5; // changing x is valid; but not (*i)` 
- `const int i=3;` and `int const i=3;` are same

### Data Type sizes
- Only long changes in 32 and 64 bits
- Int 4 & 4 bytes
- [Reference](https://docs.oracle.com/cd/E19253-01/817-6223/chp-typeopexpr-2/index.html)
- Pointers (also change) are blocks of memory (**8/4 bytes** on 64-bit/32-bit machines) that reference memory addresses of any data type in C.

### Misc
- Case insensitive string compare: `strcasecmp(s, t)`
- Illegeal Declaration:

```cpp
int size = 3;
int array[size] = {1, 2, 3}; // If not initializied, this is valid
```

### Doubts:
- Typedef
- precedence table
- Type cast order
-  Function pointer syntax
    - `` 

---
# Snippets
```
if(-394){ //anything other than 0 and even '0' is positive
        printf("true");
    }
    else{
        printf("false");
    }
```
- Output: True

```
#include <stdio.h>
int main()
{
    static int i=5;
    if(--i){
        main();
        printf("%d ",i);
    }
    return 0;
}
```
- It produces output 0000 because static variable is retained after scope and shared. 
---
```
unsigned int foo(unsigned int n, unsigned int r) { 
  if (n  > 0) return (n%r +  foo (n/r, r )); 
  else return 0; 
} 
```
- No of set bits in binary notation
---
```
#include <stdio.h>
int main()
{
    float x = 'a';
    printf("%f", x);
    return 0;
} 
```
- Produces output 97.000000 not a runtime error.
---
```
#include<stdio.h>
int main() 
{
int a=3.14;
printf("%d",a);
return 0;
}
```

- Produces output 3 not error. 
--- 
```
#include <stdio.h>
int main()
{
int y = 1;
if (y & (y = 2)) // y is assigned 2 and 2 & 2 = TRUE
    printf("true %d\n");
else
    printf("false %d\n");
}
```
- Output: True garbagevalue
---
```
#include <stdio.h>
int main()
{
    int a = 10;
    if (a == a--)
        printf("TRUE 1\t");
    a = 10;
    if (a == --a)
        printf("TRUE 2\t");
}
```
- Output: True 2
- Note: `%3d and %03d will print <space><space>1 and 001 respectively`
- Switch case can compare only `int, char or enum`
---

```cpp
#include <stdio.h>
void main()
{
    int a[2][3] = {1, 2, 3, 4, 5}; // Array init 0
    int i = 0, j = 0;
    for (i = 0; i < 2; i++)
    for (j = 0; j < 3; j++)
    printf("%d", a[i][j]);
}
```

- Output: 1 2 3 4 5 0

---

```cpp
#include <stdio.h>
#include <string.h>
void main()
{
    char *a[2] = {"hello", "hi"};
    printf("%d", sizeof(a));
    return 0;
}
```
- Output: 16
- Pointers are blocks of memory (**8/4 bytes** on 64-bit/32-bit machines) that reference memory addresses of any data type in C.

---

```c++
#include <stdio.h>
#include <string.h>
void main()
{
    char a[2][6] = {"hello", "hi"};
    printf("%d", sizeof(a));
    return 0;
}
```
Output: 12 (i.e. 2x6)

---

```cpp
#include <stdio.h>
int main()
{
    int a[4] = {1, 2, 3, 4};
    int *p = &a[1]; // void
    int *ptr = &a[2]; // void
    int n = 1;
    n = ptr - p;
    printf("%d\n", n);
}
```

Output: 1
Output for void: 4

---


