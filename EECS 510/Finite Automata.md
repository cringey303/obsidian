5-tuple:
$$M=<Q, \Sigma, δ, s, F>$$
- $Q$: States
- $\Sigma$: Alphabet (the characters the machine reads)
- $\delta$: Transition function (the rules for moving between states)
- $s$: Start state
- $F$: Final/Accepting states

Process each symbol step-by-step

Example:
- 4 states: 0,1,2,3
- instructions: a,b
	- a: advances to the next state
	- b: stays on the same state
- therefore, any set with 3 or more $a$s will be part of the language
Any set that is part of the language is called a [[Regular Sets]]

Example:
*We want to accept strings only of the form $xaaay$ where there are 3 $a$s consecutively and $x$ and $y$ can be any character*
Design the automata to reach the final state of 3 consecutive $a$s:
- 4 states: 0,1,2,3
- only $a$ advances to the next state
- any other character resets to first state
![[FiniteAutomataEg|200]]

Example:
*Want a language composed of 0s and 1s, and total characters have to be a multiple of 3.*
$$\{x \in \{0,1\}* | x\text{ has to be multiple of }3\}$$
solution: 
- 3 states: 0, 1, 2
- number of chars so far
	- 0 mod 3
	- 1 mod 3
	- 2 mod 3
	- etc
- these mods fit every number of chars
	- any multiple of 3 will fit state 0, the "final" state

[[Deterministic Finite Automata]]
[[Non-deterministic Finite Automata]]

Lemma 1
$$\hat{\}$$