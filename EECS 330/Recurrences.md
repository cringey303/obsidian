### Conventions:
- ceilings and floors don't affect recurrences

## Four Methods for solving recurrences:
- 
- recursion-tree
- master
- Akra-Bazzi


### Substitution
![[Screenshot 2026-02-02 at 10.16.34.png]]
![[Screenshot 2026-02-02 at 10.14.43.png|500]]

Example: $T(n)=4T\left( \frac{n}{2} \right)+n$
- Guess: $T(n)=O(n^2)$
- Prove: $T(n)\leq cn^2$ by induction
![[Screenshot 2026-02-02 at 10.19.05.png|600]]
