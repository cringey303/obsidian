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
- Purpose: filter r