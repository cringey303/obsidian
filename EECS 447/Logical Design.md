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