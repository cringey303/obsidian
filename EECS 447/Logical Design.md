### Contents:
[[#Data Model]]
- [[#Relational Model]]
[[#Relational Integrity Constraints]]

---
- **Conceptual Design**
	- "sketch the design"
	- subjective
- **Schema design**
	- rules to follow
	- objective

## Data Model
- Structure of Data
	- Mathematical representation of data
	- Examples: relational model = tables; semi-structured model = trees/graphs
- Operations on data
- Constraints
### Relational Model
- Simple but powerful mode
- highly efficient implementations
- RDBMS dominates the database industry
- Relational database: a set of **relations**
- A relation is a table...
	- rows: tuples or records
	- columns: attributes![[Screenshot 2026-02-03 at 12.59.29.png|520]]
- Relation
	- **<span style="color:rgb(240, 76, 164)">Schema</span>**: specifies name of relation, plus name and type of each column.
		- Students (sid: string, name: string, login: string, age: integer, gpa: real)
		- Car (vin: string, make: string, model: string, year: integer, state: string, platenumber: string)
	- **<span style="color:rgb(240, 76, 164)">Instance</span>**: a table, with rows and columns.
		- \#rows = *cardinality*
		- \#fields/columns = *degree*
			- number of attributes
- ![[Screenshot 2026-02-03 at 13.05.07.png|500]]
- ![[Screenshot 2026-02-03 at 13.05.57.png|500]]
	- use commas for attributes

![[Screenshot 2026-02-03 at 13.06.31.png|500]]
- Tuples in a relation are *not* considered to be ordered, even though they appear to be in the tabular form
- all values are considered *atomic* (indivisible)
- A *<span style="color:rgb(0, 176, 240)">special null value</span>* is used to represent values that are unknown or inapplicable to certain tuples
---
## Relational Integrity Constraints
- Constraints are *conditions* that must hold on *all* valid relation instances. There are three main types of constraints:
	1. Domain constraints
		1. the value of an attribute must come from its domain
	2. Key constraints
	3. Referrential integrity constraints
	![[Screenshot 2026-02-03 at 13.15.11.png|250]]  ![[Screenshot 2026-02-03 at 13.15.27.png|350]]

---
## Primary Keys
- A set of attributes is a *candidate key* for a relation if:
	1. No two distinct tuples can have same values in all key fields, and
	2. This is not true for any subset of the key.
		- Only condition 1? A <span style="color:rgb(0, 176, 240)"><i>superkey</i></span>
- A candidate key is sometimes called a <span style="color:rgb(0, 176, 240)"><i>minimal superkey</i></span>
- The set of all attributes is a superkey
- If there's > 1 key for a relation, one of the keys is chosen (by DBA) to be the *primary key*

### Foreign Keys, Referential Integrity

### Translating entity sets
- attributes -> columns
- key attributes -> primary key