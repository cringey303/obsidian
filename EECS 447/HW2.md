Exercise 3.3.1 (b)-(e) (Textbook Page 92) 
# R(A,B,C,D)
### a. 
FDs:
- AB → C
- C → D
- D → A
- C → A
Candidate keys:
- {A,B}
- {B,D}
- {B,C}
<span style="color:rgb(240, 76, 164)">BCNF violations:</span>
- C→D
- D→A
- C→A
<span style="color:rgb(240, 76, 164)">Decompose:</span>
using C→D
- $R_{1}(C,D)$
- $R_{2}(C,A,B)$
	- check for more violations with FDs:
		- AB→C
		- C→A (violation)
			- $R_{2}(A,C)$
			- $R_{3}(C,B)$
so:
- $R_{1}(C,D)$
- $R_{2}(A,C)$
- $R_{3}(C,B)$

### b.
FDs: 
- B→C
- B→D
Candidate key:
- {A,B}
<span style="color:rgb(240, 76, 164)">BCNF violations:</span>
- B→C
- B→D
<span style="color:rgb(240, 76, 164)">Decompose:</span>
$R_1$ contains all attributes in violation
$R_{2}$ contains B (left-hand side) and everything else (only A is left)
**$R_{1}(B,C,D),R_{2}(A,B)$

### c.
FDs: 
- AB→C
- BC→D
- CD→A
- AD→B
- AB→D
Candidate key:
- {A,B}
- {B,C}
- {A,D}
- {C,D}
<span style="color:rgb(240, 76, 164)">BCNF violations:</span>
- none
<span style="color:rgb(240, 76, 164)">Decompose:</span>
nothing to decompose

### d.
FDs: 
- A→B
- B→C
- C→D
- D→A
- A→C
- A→D
- B→A
- B→D
- C→A
- C→B
Candidate key:
- A
- B
- C
- D
<span style="color:rgb(240, 76, 164)">BCNF violations:</span>
- none
<span style="color:rgb(240, 76, 164)">Decompose:</span>
nothing to decompose


# R(A,B,C,D,E)
### e.
FDs: 
- AB→C
- DE→C
- B→D
Candidate key:
- {A,B,E}
<span style="color:rgb(240, 76, 164)">BCNF violations:</span>
- none
<span style="color:rgb(240, 76, 164)">Decompose:</span>
nothing to decompose