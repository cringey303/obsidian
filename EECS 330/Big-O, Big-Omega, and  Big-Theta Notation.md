## Informally:
### O-notation 
characterizes an upper bound on the asymptotic behavior of a function
- It says that a function grows no faster than a certain rate.
- This rate is based on the highest-order term.
- eg $7n^3+100n^2-20n+6$ is *$O(n^3)$ since the highest order term is $7n^3$, therefore that is the fastest it can grow
### o-notation
characterizes a strict upper bound on the asymptotic behavior of a function
- O-notation: $\leq$
	- no faster than
- o-notation: $<$
	- *strictly* less than
	- $\lim_{ n \to \infty } \frac{f(n)}{g(n)} = 0$; e.g. $\lim_{ n \to \infty } \frac{n^{1.9999}}{n^2} = \lim_{ n \to \infty } \frac{1}{n^{0.0001}}$
### $\Omega$-notation 
characterizes the lower bound of the asymptotic behavior
- since the highest order term is $7n^3$, the slowest it can grow is also $n^3$
### $\omega$-notation
strict lower bound
- $\Omega$-notation: $\geq$
	- at least as fast as
- $\omega$-notation: $>$
	- strictly faster than
	- $\lim_{ n \to \infty } \frac{f(n)}{g(n)} = \infty$
### $\Theta$-notation
If a function has the same lower and upper bounds of $g(n)$ (O($g(n)$) and $\Omega(g(n))$), then you can claim $\Theta(g(n))$ 

### Comparison of functions
![[Screenshot 2026-01-30 at 10.21.57.png|400]]
Note: some things work for real numbers, but not for functions.
e.g. one must be true: $a\leq b, b\geq a$, however not true for oscillating functions 
## Formally:
O-notation: $0\leq f(n) \leq cg(n)$ for all $n \geq n_{0}$
$\Omega$-notation: $0\leq cg(n) \leq f(n)$ for all $n \geq n_{0}$
$\Theta$-notation: $0\leq c_{1}g(n)\leq f(n) \leq c_{2}g(n)$ for all $n \geq n_{0}$

There exists positive constants $c$ and $n_{0}$, such that for all $n\geq n_{0}$​, the following inequality holds:
$$0\leq c⋅g(n)≤f(n)$$
Prove $f(n) = \Omega(g(n))$ where 
- $f(n) = 3n^3+5n^2-7$ 
- $g(n) = n^3$


find $c*n^3 \leq 3n^3 + 5n^2 - 7$ 

---
### Correct use of asymptotic notation:
- O-notation is NOT $\Theta$-notation
- _cannot say_: $O(n\log n)$-time algo runs faster than an $O(n^2)$-time algo. 
- best to say: the running time is $\Theta(n^2)$.
- could say: running time is $\Theta(n^3)$, but that's less precise

---
### Asymptotic growth of functions
![[Screenshot 2026-01-30 at 10.28.59.png]]
- base of logs DON'T matter asymptotically
- base of an exponential and the degree of a polynomial or polylog DO matter asymptotically

### Notational convention
![[Screenshot 2026-01-30 at 10.32.12.png|400]]
