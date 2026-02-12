NFA
Multiple possible transition types for the same input, allowing them to exist in several states at once.

$$M=<Q, \Sigma, δ, S, F>$$
Q: state
$\delta$: 
S: set of states
F: Final states

A = $\{x \in {0,1}*| 5th \text{ from right is }1\}$
$0010110 \in A$ , $100110 \not\in A$
![[NFA]]
in this case:
Q: $\{ A,B,C,D,E,F\}$
$\Sigma$ = $\{0,1\}$
- $\delta(A,0) = A$
- $\delta(A,1) = A$
- $\delta(A,1) = B$
$S = \{A\}$
$F = \{F\}$

NFA goes through all possible outputs. If final state is in the set of outputs, then, the machine will accept that input.
For 100110, since when the machine reaches the last 0 one of its states is at F already, that F will just be discarded.