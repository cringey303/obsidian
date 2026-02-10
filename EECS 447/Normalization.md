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
- a FD has the form X→Y, where X and Y are sets of attributes in a relation R
- X → Y means that whenever two tuples in R agree on all attributes in X, they must also agree on all attributes in Y
	- example: SID → name, account; CID → Cname, location
- Trivial FD: $X→Y$ is trivial if Y is a subset of X

### Rules of FDs
- Armstrong’s axioms
	- Reflexivity: if Y is a subset of X, then X → Y
	- Augmentation: if X → Y, then XZ → YZ for any Z
	- Transitivity: if X → Y and Y → Z, then X → Z
- Rules derived from axioms
	- Splitting: if X → YZ, then X → Y and X → Z
	- Combining: if X → Y and X → Z, then X → YZ

### First Normal Form
- It’s a table
	- every row-and-column intersection contains exactly one atomic value from the applicable domain
- A primary key is enforced
	- no duplicate rows
	- rows are identified by primary key
	- columns are identified by attribute name
	- values are accessed by identifying primary key of the tuple and the attribute name

### Second Normal Form
- in first normal form
- every non-prime attribute is fully dependent on a candidate key
	- an attribute is prime if it is a member of any candidate key