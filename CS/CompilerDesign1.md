## Errors
#### Types
- Compiler errors
    - Lexical 
    - Syntax
    - Semantic
- Linker errors
- Preprocessor errors
- Runtime errors
#### During compilation
- Preprocessor errors
- Compiler errors
- Linker errors
- *Note: Logical errors can't be found.*
---
#### Symbol Table
- Data structure modified and accessed in all phases
- Eg: line number, type (semantic phase), offset, address(machine code), etc 
---
### Clarifications with terms
- Parse tree, semantic tree (anotated parse tree)
- Syntax tree

---
## Lexical Analyser
- *Input*: Character stream
- *Output*: Token stream or errors
- Removes all comments and whitespaces 
- Finite automata is used to design
### Other names
- Scanner, Token recogniser, Token generator, Linear Phase, First phase of compiler
### Tokens
- Keyword, Operators, Identifiers, Constants/ Literals, Special symbols (punctuation)
- ***Note: "string_ex", ++, ==, +=, && are single token whereas * * is 2 different tokens*** 
- *Don't count comments*
- Eg: `int 1x;` is invalid as *identifier starts with alphabet or underscore*
### Functions
- Token recogniser and generator, removes comments and whitespace
- Produces lexical errors 
- Largest prefix rule (maximal munch)
---
## Syntax Analysis
- *Input:* Token string
- *Output:* Parse tree and syntax error if any
### Other names
- Syntax verifier, Parse tree generator, second phase
### Syntax error vs Syntactic error
- Sometimes, no lexical errors, can also lead to syntax error. 
- ***; missing - (parse tree can not be generated)*** 
- **Syntactic error**( *Syntax or Semantic error*)
    - `fro(i=0,i<n,i++);` - Semantic error not syntax error
    - fro is valid function call syntax 
    - if fro definition prototype or #include headers are available -- ***No semantic error also*** 
- `if()` or `while()` or `switch()`  error - Missing expression
    - `for(;;)` allows empty expression => *by default true* 
---
### Types of parsers

1. ***Top-Down parsers***
    1. *LL(0)*
    1. *LL(1)*  *predictive parser*
    1. *Others...*
1. ***Bottom-UP parsers***
    1. *LR* 
        1. LR(0)
        1. SLR(1)
        1. LALR(1)
        1. CLR(1) *also known as LR(1)*
    - ***LR(0) ⊆ SLR(1) ⊆ LALR(1) ⊆ CLR(1)*** 
    1. *Operator Precedence Parser*
1. Others....
---
### Top down parsers Types:
1. Recursive descent 
    - Procedure for every production
1. Non recursive descent
    - Table implemented (Stored CFG)
---
### LL(1) parser
- can be implemented by both recursive and non recursive
- Usually non recursive (by default) - *table driven parser*
- Predictive parser
    - L = *left to right*
    - L = *Left most derivation*
    - (1) = *one token at a time*
- Steps: 1. Write grammar 2. Build table 3. Implement LL(1) algorithm
### LL(1) grammar
- Unambiguous grammar
- Eliminate Left recursion
    - Possibility of entering infinite loop
    - Left to right recursion conversion
    - **`S -> Sa | b `**
        - **`S -> bS' and S' -> aS' | ^ `**
- Left factoring



