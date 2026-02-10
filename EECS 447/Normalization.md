- Fix bad designs
- A systematic approach to
	- avoid inconsistency
	- avoid redundancy

Topics
- redundancy
- functional dependancy
- decomposition
- Boycd-Codd normal form (BCNF)

Redundancy:
![[Screenshot 2026-02-10 at 12.40.58.png]]

instead, have 3 tables: class, student, and relationship relation table

**Unnecessary decomposition**: separating into different tables when unnecessary![[Screenshot 2026-02-10 at 12.53.39.png]]

**Bad decomposition**: ![[Screenshot 2026-02-10 at 12.54.49.png]]

Functional dependencies:
- a FD has the form X->Y, where X and Y are sets of attributes in a relation R
- X -> Y means that whenever two tuples in R agree on all attributes in X, they must also agree on all attributes in Y
	- example: SID -> name, account; CID -> Cname, location
	- 