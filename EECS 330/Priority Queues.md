- Application of heap to use it as an efficient primary queue
- A **max-priority queue** supports the following operations:
	- $Insert(S,x,k)$: inserts element $x$ with key $k$ into set $S$.
	- $Maximum(S)$: returns element of $S$ with largest key
	- $Extract-Max(S)$: removes and returns element of $S$ with largest key.
	- $Increase-Key(S,x,k)$: increases value of element $x$’s key to $k$. Assumes $k\geq x$’s current key value

**Maximum** operation
- Max-heap-maximum implements the MAXIMUM(S) operation, which returns the element of set S with te largest key, i.e., the first element of the heap A[1].
- Running time: $\Theta(1)$![[Screenshot 2026-02-13 at 10.28.37.png]]

**Extract-Max** operation
- Max-heap-extract-max extra