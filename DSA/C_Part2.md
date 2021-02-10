### Some points to remember
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



### Doubts:
- Typedef
- precedence table
- Type cast order
-  Function pointer syntax
    - `` 

---
# Snippets
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
```
unsigned int foo(unsigned int n, unsigned int r) { 
  if (n  > 0) return (n%r +  foo (n/r, r )); 
  else return 0; 
} 
```
- No of set bits in binary notation