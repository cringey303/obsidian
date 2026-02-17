$$M = <Q,\Sigma, \delta, s, F>, s \in Q$$
$$N = <Q,\Sigma, \Delta, S, F>, s \subseteq Q$$
S: $Q\times \Sigma \to Q$
$\Delta$: $Q\times \Sigma \to 2^Q$
$2^Q=\{A|A\subseteq Q\}$
$\hat{\Delta}:Q\times \Sigma^* \to 2^Q$
$\hat{\Delta}(A, \in)=A$

$$\hat{\Delta}(A, xa) = \bigcup_{q \in \hat{\Delta}(A, x)} \Delta(q, a)$$
- $\hat{\Delta}(A,xa)$: The set of states the NFA can be in after starting in set A and reading the entire string $xa$.
- $\hat{\Delta}(A,x)$: First, the machine processes the string x. This results in a set of intermediate states.
- $q \in \hat{\Delta}(A, x)$: We look at every individual state q that the machine could possibly be in after reading x.
- $\Delta(q,a)$: From each of those states q, we see where the machine goes when it reads the final character a.
- $\bigcup$: We take the union of all those resulting sets to find the final collection of possible states.


