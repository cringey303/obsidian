## Informally:
### O-notation 
characterizes an upper bound on the asymptotic behavior of a function
- It says that a function grows no faster than a certain rate.
- This rate is based on the highest-order term.
- eg $7n^3+100n^2-20n+6$ is *$O(n^3)$ since the highest order term is $7n^3$, therefore that is the fastest it can grow
### $\Omega$-notation 
characterizes the lower bound of the asymptotic behavior
- since the highest order term is $7n^3$, the slowest it can grow is also $n^3$
### $\Theta$-notation
If a function has the same lower and upper bounds of $g(n)$ (O($g(n)$) and $\Omega(g(n))$), then you can claim $\Theta(g(n))$ 

