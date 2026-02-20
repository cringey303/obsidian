Exercise 3.3.1 (b)-(e) (Textbook Page 92) 
# R(A,B,C,D)
### a. 
FDs:
- 
Candidate keys:
-  
<span style="color:rgb(240, 76, 164)">BCNF violations:</span>
- 
<span style="color:rgb(240, 76, 164)">Decompose:</span>
- 
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
# R(A,B,C,D,E)