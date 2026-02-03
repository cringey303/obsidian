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
	- **Schema**: specifies name of relation, plus name and type of each column.
		- Students (sid: string, name: string, login: string, age: integer, gpa: real)
		- Car (vin: string, make: string, model: string, year: integer, state: string, platenumber: string)
	- **Instance**: a table, with rows and colunm