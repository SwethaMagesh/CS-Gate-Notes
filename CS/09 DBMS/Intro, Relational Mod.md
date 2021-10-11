**Types of lang**
- DDL
- DML
- DCL (Grant, Revoke)
- TCL (Commit, Rollback)


**3 LEVELS**
- PHY LEVEL -> CONCEPTUAL LEVEL -> EXTERNAL LEVEL
- Physical data independence (relatively easy) and Logical data independence

**Tiers**
  - 2 Tier : app client and server
  - 3 Tier : server, server, database system
![image](https://user-images.githubusercontent.com/43994542/134869817-098cf8e9-0652-4319-aba3-d1e936a6dde4.png)

---
**ER Diagrams**
- Diagramatic representation of how data is related

**Entity Type**
- Eg: STUDENT, COURSE


**Entity**
- EG: S1 in Student entity


**Entity Set**
- Collection of all entities in entity type


**Attibute**
- Properties of entity type
- Composite (Eg: Address -> street, city, country) 
- Multivalued( Eg: phone num) - _Double oval_
- Derived (Eg: Age) - _Dotted oval_


**Relationship type and relationship set**
- Degree of relation : unary, binary, ternary
- Unary (Eg: PERSON - married to )
- Binary (Eg: STUD - enrolled - COURSE)

**Cardinality of relationship**
- ONE - ONE
- MANY - ONE
- MANY - MANY
- **GFG NOTATIONS: Arrow - one side only**


**Participation Constraint**
- Total Participation (Double line) - all entities must participate


**Weak entity Type and Identifying relations**
- Weak entity type - _Denoted by double rectangle_
- Key attribute cannot be defined. Cannot exist without another entity type
- Eg: DEPENDENTS Relation in company 
- **Always total participation**
- The relationship between weak entity type and its identifying strong entity type is called **identifying relationship** and it is represented by double diamond.

---
**Recursive relations**
- relation between similar entity types (unary)
- entities have different roles
- Eg: Supervisor and subordinate
- **NOTE:** Take care of min and max cardinality 
---
**DOUBT: Verify the rules (not so clear in GFG)**
- ONE to ONE - Bring to total participation side (only 1 table required) ; else atleast 2 tables required.
- MANY to ONE - Bring from ONE to MANY side
- MANY to MANY - Requires 3 tables ; cannot minimise to 2 tables


**ER notations**


![image](https://user-images.githubusercontent.com/43994542/135228369-b7fd4f26-6b70-4104-9a3a-a478bc1c6e65.png)

---

Enhanced entity-relationship diagrams
- Sub Class and Super Class; Specialization and Generalization; Union or Category; Aggregation
- Specialized classes are often called **subclass** while a generalized class is called a **superclass** -> “IS-A analysis”
- Arrow direction: SUPER -> SUB
- **TOTAL AND PARTIAL**
- **OVERLAPPED AND DISJOINT**
- **Multiple inheritance** = Eg: A faculty in a university system can be a subclass of Employee and Alumnus
- **Doubt:** UNION vs SUBCLASS 
---



