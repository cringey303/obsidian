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

### Third Normal Form
- in 2NF
- every non-prime attribute is non-transitively dependent on a candidate key
- transitive dependency
	- A→B, B is not a candidate key
	- B→C
	- C is transitively dependent on A

### Boyce-Codd Normal Form (BCNF)
- A relation R is in BCNF if
	- for every non-trivial FD X→Y in R, X is a superkey
	- That is, all non-trivial FDs follow form “key → other attributes”
- Or
	- a relation R is in BCNF iff every non-trivial determinant is a candidate key

**3NF vs. BCNF**
- 3NF but not BCNF
	- exist a non-trivial FD X→Y, X is not a super key, and Y is a subset of a candidate key
		- YZ → A (any attribute)
		- X → Y, therefore: XZ → YZ
		- XZ → YZ → A
		- XZ is also a candidate key
- example of 3NF but not BCNF
	- in a relation r(Z, X, Y) where ZX and XY are candidate keys
	- If we also have X → Y
	- 3NF: Yes
	- BCNF: No
		- because X is not a superkey

### Decomposition to BCNF
1. Identify candidate keys
2. Find a BCNF violation
	- A non-trivial FD $X→Y$ in $R$ where $X$ is not a superkey of $R$
3. “Grow” $Y$ to include all the attributes determined by $X$
4. Decompose $R$ into $R_1$ and $R_{2}$, where
	1. $R_1$ has attributes $X \cup Y$
	2. $R_2$ has attributes $X\cup Z$, where Z contains all attributes of R that are in neither X nor Y (i.e. $Z - attr(R)- X -Y$)


![[Screenshot 2026-02-17 at 13.07.38.png|550]]
