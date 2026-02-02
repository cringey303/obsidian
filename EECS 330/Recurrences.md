### Conventions:
- ceilings and floors don't affect recurrences

# Four Methods for solving recurrences:
- subsitution
- recursion-tree
- master
- Akra-Bazzi


---
## Substitution method
![[Screenshot 2026-02-02 at 10.16.34.png|550]]
![[Screenshot 2026-02-02 at 10.14.43.png|500]]

Example: $T(n)=4T\left( \frac{n}{2} \right)+n$
- Guess: $T(n)=O(n^2)$
- Prove: $T(n)\leq cn^2$ by induction (ATTEMPT 1)
![[Screenshot 2026-02-02 at 10.19.05.png|600]]
- Prove: $T(n)\leq c_{1}n^2-c_{2}n$ by induction (ATTEMPT 2)
![[Screenshot 2026-02-02 at 10.24.12.png|550]]
---
## Recursion tree method
- A recursion tree models the running time of a recursion
	- each node represents the cost of a single subproblem somewhere in the recursive functions
- Can be unreliable
- Not formal proof
	- Use recursion tree to generate a guess
	- use sub method to prove the guess

Example: $T(n)=3T\left( \frac{n}{4} \right)+\Theta(n^2)$
![[Screenshot 2026-02-02 at 10.28.55.png]]

Total # of leaves: $3^{height} = 3^{\log_{4}n} = n^{\log_{4}3}$
![[Screenshot 2026-02-02 at 10.35.23.png]]

---
## Master method
Provides a "cookbook" method for solving algorithmic recurrences of the form where $( a>0,b>1)$ $$T(n)=aT\left( \frac{n}{b} \right)+f(n)$$Note: in general, $a$ and $b$ may not be equal

