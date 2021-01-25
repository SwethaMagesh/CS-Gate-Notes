### Functional Dependency
- In general, a functional dependency α → β always holds- If either all values of α are unique or if all values of β are same or both.
- Types: Trivial and Non trivial (RHS is subset of LHS)
### Canonical cover
- Irreducible set
- ***Step1:*** Split RHS individually. Find closure with and without each FD to determine if it is essential. Eliminate unnecessary
- ***Step2:*** If LHS has more than 1 attribute, then try to reduce that too.
### Candidate key
- Essential attributes are those attributes which are not present on RHS of any functional dependency.
- **Essential attributes** are always a part of every candidate key.
- *Case 1:* If all essential attributes together can determine all remaining non-essential attributes, then- 
**The combination of essential attributes is the candidate key.**
**It is the only possible candidate key.**
- *Case 2:* In this case, multiple candidate keys are possible. To find the candidate keys, we check different combinations of essential and non-essential attributes.
- ***Note: Number of superkeys is a combinatorial question*** 
---

### Normalisation 
#### 1NF
A given relation is called in First Normal Form (1NF) if each cell of the table contains only an atomic value.ie.  if the attribute of every tuple is either single valued or a null value.
#### 2NF 
- `1NF and no partial dependency`
#### 3NF 
- Every A-> B, no transitive dependency
```
- Either A is superkey
- Or B is prime attribute
```
- Non prime should not determine non prime
#### Boyce-Codd Normal form (BCNF)
- `Every A-> B, A is a superkey`
- BCNF - often lossless decomposition difficult and dependencies might not be preserved
#### 4NF
- `NO multivalued dependency` ( different from multivalued attribute)
- R(Eid, Phone1, Phone2, Phone3, Email1, Email2)
#### 5NF
- `No join dependency`
- All joins must be lossless joins (no spurious tuples generated during join)
---
#### A Note on Lossless and lossy decomposition
- ***Lossless decomposition and non additive join*** 
> - All tuples retained in decomposition
> - No spurious tuple generated.
- ***Dependency preservation*** - All subrelations should satisfy the FD, and none of FDs should be lost
- *Note: Lossy joins are also called careless joins*
---
- ***Conditions for a lossless decomposition***
- If R is split into R1, R2,,
- `R1 U R2 = R`
- `R1 ⩃ R2 not NULL (There must be common attribute`
- ` Common attribute must be super key of either R1 or R2 or both`   
- To prove for more subrelations, consider one step at a time, each having 2 Subrelations
---


# Doubts
- Transaction
- Concurrency
    - Locks and Timestamp based
- Relational and Tuple calculus
- Indexing File 
