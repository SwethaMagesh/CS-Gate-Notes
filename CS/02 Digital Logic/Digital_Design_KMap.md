## Don't care
- A Don’t Care cell can be represented by a cross(X) in K-Maps representing a invalid combination. 
- While forming groups of cells, we can consider a “Don’t Care” cell as 1 or 0 or we can also ignore that cell
## KMap - Karnough Map Rules
- No zeros allowed.
- No diagonals.
- Only power of 2 number of cells in each group.
- Groups should be as large as possible.
- Every one must be in at least one group.
- Overlapping allowed.
- Wrap around allowed.
- Fewest number of groups possible.
## Implicants
- Prime implicants
- Essential prime implicants
- Redundant prime implicants
- Selective prime implicants
## In a dual function
- AND operator of a given function is changed to OR operator and vice-versa.
- A constant 1 (or true) of a given function is changed to a constant 0 (or false) and vice-versa.
## Self duals
- A function is said to be Self dual if and only if its dual is equivalent to the given function, i.e., if a given function is 
`f(X, Y, Z) = (XY + YZ + ZX)` then its dual is, `fd(X, Y, Z) = (X + Y).(Y + Z).(Z + X)` 
- `(fd = dual of the given function) = (XY + YZ + ZX)`, it is equivalent to the given function. So function is self dual.
- Now, lets check number of Self dual functions possible for a given function.
Let, a function has n variables then,
 ***Number of pairs possible = 2<sup>n</sup>/2 = 2<sup>(n-1)</sup>***
- Therefore, number of Self dual functions possible with n variables
= ***2<sup>2(n-1)</sup>***
There are 2 possibilities for each pair.
- ***Note:***
- Every Self dual function is neutral but every neutral function is not Self dual.
- Self duality is closed under compliment i.e, compliment of a Self dual function is also Self dual.
## SOP AND POS
#### *Always remember POS ≠ (SOP)’*
#### *The correct form is (POS of F)=(SOP of F’)’*
- Minterms - Product terms - 1's - used in SOP - Take as such 
- Maxterms - Sum terms     - 0's - used in POS - Take complements
