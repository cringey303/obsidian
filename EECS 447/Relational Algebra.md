Based on operators:
- core set of operators:
	- selection
	- projection
	- cross product
	- union
	- difference
	- renaming
- additional, derived operators
	- join
	- natural join
	- intersection
	- etc
- Compose operators to make complex queries![[Screenshot 2026-02-19 at 12.47.35.png|550]]

## Single-table operations
### Projection
- input: a table R
- notation: $\pi_{L}R$
	- L is a list of columns in R
- Purpose: select columns to output
- Output: same rows, but only the columns in L
	- number of rows may be less (depends on where we have duplicates or not)
- ![[Screenshot 2026-02-19 at 12.53.54.png|550]]

### Selection
- input: a table R
- Notation: $\sigma_{p}R$
	- $p$ is called a selection condition/predicate
- Purpose: filter rows according to some criteria
- Output: same columns as $R$, but only rows of $R$, that satisfy $p$![[Screenshot 2026-02-19 at 12.56.17.png|550]]

### Renaming
- input: a table R
- Notation: $\rho_{S}R,\rho_{(A_{1},A_{2},\dots)}R\text{ or } \rho_{S(A_{1},A_{2},\dots)}R$
- Purpose: rename a table and/or its columns
- Output: a renamed a table with the same rows as $R$
- Used to 
	- avoid confusion caused by identical column names
	- create identical columns names for natural joins![[Screenshot 2026-02-19 at 13.00.23.png|550]]

## Many tables operations
### Union
- Input: two tables R and S
- Notation: $R\cup S$
	- R and S must have identical schema
- Output:
	- has the same schema as R and S
	- contains all rows in R and all rows in S, with duplicate rows eliminated

### Difference
- Input: R and S
- Notation: $R-S$
	- R and S must have identical schema
- Output:
	- same schema as R and S
	- contains all rows in R that are not found in S

### Intersection

### Cross product
- Input: R and S
- notation: $R  S$
- Purpose: pairs rows from two tables
- output: for each row $r$ in $R$ and each row $s$ in $S$, output a row $rs$ (concatenation of $r$ and $s$)
	- that is, pair each row in 