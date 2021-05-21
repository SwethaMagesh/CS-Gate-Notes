## Relations, functions
- Some intuitions for count of functions
### Assymmetric Relations
- Diagonal always 0. No 1-1 pair in symmetric places
- `0-1, 1-0, 0-0` for (`n`<sup>`2`</sup>`-n)/2`
- Eg: `R={(a,b)| a<b}`
### Antisymmetric Relations
- Diagonal may or may not be 1.
- Eg: `R={(a,b)| a<=b}` 
- *less than, less than equal, equal to*
- ***All asymmetric relations are antisymmetric*** 
<img src="https://user-images.githubusercontent.com/43994542/106768586-0dd7b280-6662-11eb-8b01-939004521350.png" height=100>


---

### Transitive Relations
- Check methodically 
- *less than, less than equal, equal to*
- ***Trick:*** 
    - One element in R or if non diagonal entry along with diagonal - transitive only
---
### Partial Ordering Relation
- Reflexive, Antisymmetric, Transitive
---
## Functions
- Size of function set is always ***Size of domain*** 
- *One-one* - Injective
- *Onto*    - Surjective
- Bijective: **f and f<sup>-1</sup> exists**
- Composition: g ∘ f : X → Z, defined by (g ∘ f )(x) = g(f(x)) , where g :Y → Z, f:X → Y
---
## Important note
Relations And Functions
- |A| = m and |B| = n, then
1. No. of functions from A to B = n<sup>m</sup>
2. No. of one to one function = (n, P, m)
3. No. of onto function =nm – (n, C, 1)*(n-1)<sup>m</sup> + (n, C, 2)*(n-2)<sup>m</sup> …. +(-1)<sup>m</sup>*(n, C, n-1), if m >= n; 0 otherwise
4. Necessary condition for bijective function |A| = |B|
5. The no. of bijection function =n!
6. No. of relations =2<sup>mn</sup>
7. No. of reflexive relations =2<sup>n(n-1)</sup> 
8. No. of symmetric relations = 2<sup>n(n+1)/2</sup> 
9. No. of Anti Symmetric Relations = 2<sup>n</sup>*3<sup>n(n-1)/2</sup>
10. No. of asymmetric relations = 3<sup>n(n-1)/2</sup>
11. No. of irreflexive relations = 2<sup>n(n-1)</sup>
---
## Algebraic Structures
- **Closure**
- **Semigroup**
- **Monoid**
- **Group**
- **Abelian group**
- Satisfies Closure, Associative, Identity, Inverse, and Commutativity

<img src="https://user-images.githubusercontent.com/43994542/106772590-2d70da00-6666-11eb-8f09-25d2b81893b7.png" height=200>

##### Some Examples
```
- (Square Matrices, x ) - Monoid, (inverse doesn't exist for singular matrices)
- (Non-singular Matrices, x) - Group, (inverse exists)
- (Q, /) - Not closed, (a/0 doesn't belong to Q)
- (Q, x) - Monoid, (no inverse for 0)
```
- Without identity, inverse cannot exist
- Associativity - Left to right and right to left
- Identity - Right identity and left identity
    - `a * e = e * a = a` 
---
### Doubts:
- Sublattices
- Subgroups
---
### NOTE:
- Operator is a function. All operations are functions, converse is not true

![image](https://user-images.githubusercontent.com/43994542/106771615-2bf2e200-6665-11eb-93a4-4843f0f58d29.png)
- Consider (Q, +) etc for identifying group or not?
---

## POSET
- Short representation of PO relation
- DAG - Hasse diagram 
- Upward arrow, denoting relation
- We never represent ***self loop (diagonal) and transitive edges (triangles)*** 
- Eg: 3 edges => can represent even 8 elements in Relation
### Elements of POSET
- Minimal - *no predecessor*
- Maximal - *no successor*
- Minimum / Least - *Predecessor to every element in diagram*
- Maximum / Greatest - *Successor to every element in diagram*
- Upper bound and Lower bound for a particular subset
- GLB and LUB - may or maynot exist, unique (only 1 if exists)
---

## Lattice 
- Every 2 elements say a and b must have GLB and LUB
- GLB => Meet => a∧b
- LUB => Join => avb
- ***Note: Not lattices identification*** 
- *Real life application: Code optimisation and data flow analysis. Program to lattice conversion*
---
### TYPES of lattices
#### Finite
- Finite no of elements
- Bounded lattice
#### Infinite
- Infinite no of elements
- GLB, LUB for every pair of elements and GLB, LUB doesn't exist for the entire diagram
- ***Eg: (N,<=)*** 
#### Bounded 
- Upper and Lower bound exists
- All finite and some infinite lattices
#### Complemented
- Bounded lattice
- Every element must have atleast one complement
- a and b are complements if *meet(a,b)=LUB and join(a,b)=GLB*
#### Distributed
- Bounded lattice
- If complements exist, it must be unique
- No of complements can be atmost one
#### Boolean 
- Distributed and Complemented 
- Every element has exactly 1 complement
<img src="https://user-images.githubusercontent.com/43994542/106778738-4bd9d400-666c-11eb-9e78-3baf43f076fd.png" width=300 height=300>







