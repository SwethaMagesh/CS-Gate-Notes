### Relational Model
- Relational Model was proposed by E.F. Codd to model data in the form of relations or tables. 
- Design the conceptual model in ER, convert into Relational model and implement using RDBMS like Oracle SQL, MySQL etc.
## Terms
- Attributes - properties of relation
- Tuple - Each row of a relation
- Relation Instance - The set of tuples of a relation at a particular instance of time 
- Degree - The number of attributes in the relation 
- Cardinality - The number of tuples in a relation 

## Constraints in Relational Model
- Domain Constraints - attribute level (min and max)
- Key Integrity -  a key has two properties: It should be unique for all tuples. It can’t have NULL values.
- Referential Integrity - When one attribute of a relation can only take values from other attribute of same relation or any other relation

## KEYS
- Super keys - Superset of attributes
- Candidate keys - They can uniquely identify a tuple in relation

## Anamolies due to referential integrity
- Insert anamoly
- Delete anamoly 
	- ON DELETE CASCADE
	- Remember that u have to recursively delete until all have references. 
	
- Update anamoly
	- ON UPDATE CASCADE

### Relational Algebra
- Projection (π) - removes duplicate by default
- Selection (σ)
- Rename ρ(a/b)R will rename the attribute ‘b’ of relation R by ‘a’.
- UNION (U)
- Set difference (-)
- Cross Product (X)

- JOINS:
	- Natural Join
	- Conditional Join
	
- PYQ related
	- [Q1](https://www.geeksforgeeks.org/gate-gate-cs-2012-question-50/)
		- `(A∪B)⋈A.Id>40∨C.Id<15C =  (A.Id>40((A∪B)×C)) ∪  (C.Id<15((A∪B)×C))`
	- [Q2](https://www.geeksforgeeks.org/gate-gate-cs-2012-question-43/)
		- 
### Keys
- Doubt - No of candidate keys in a Relation are nC(floor(n/2))? Why?
- Candidate keys are super keys but not vice versa
- Brush the concepts of keys from the other markdown file of '21
