Proofs should work in a general case, ie instead of a specific vector in a proof it should be an algebraic vector that is specific. Instead of being stuck in a specific dimension, we should expand to multiple dimensions if the proof is tackling that. 

If n is an even integer, then $n^2$ is even
## Direct proof
Let $n$ be an even integer. Then $n$ can be written $n = 2k$ for some integer k. Then $n^2$ = $4k^2 = 2(2k^2)$ which must be even.
#Direct_proof

## Proof by contradiction
Let n be an even integer and assume, for the sake of contradiction, that $n^2$ is odd. Since n is even, n = 2k for some integer k. Then $n^2 = 4k^2 = 2(2k^2)$ . However, this requires that  
#Proof_by_contradiction 


the magnitude of a vector is $$
\sqrt{ n_{1}+n_{2}+ \dots{} n_{n}}
$$ for any positive set of ns' $\in \mathrm{Re}$. The sum of positive numbers can never be zero. Thus, a b and c must be zero for the magnitude to be zero.

### if and only if
requires every statement to have $\Leftrightarrow$ .
I.E.


## Proof by induction
In a proof by mathematical induction, we prove the statement is true for a base case and then all the cases 

suppose u1 u2 ... uk are a set of vectors in Rn that are all orthogonal to $\vec{v}\in R^{n}$ with k<= n. Then v is orthogonal to any linear combination o

Base case (k-1): any linear combination of one vector can be written $c_{1}\vec{u_{1}}.$ then ($c_{1}\vec{v_{1}}$) $\cdot$ v - $c_{1}\cdot(\vec{u_{1}}\cdot\vec{v_{1}})$ = 0 so they are orthogonal.

Inductive hypothesis: Assume the statement is true for k = j, j $\leq n-1$ 
inductive step($j\to j+1$): suppose that all vectors $u_{j}$ are orthogonal to $\vec{v}$ consider any linear combination, which we can write. 
$$
\begin{align}
\vec{v}\cdot(c_{1}\vec{u_{1}} \dots c_{j}\vec{v_{j}} + c_{j+1}\vec{v_{j+1}} )\\

\end{align}
$$

#Proofs

see next: [[Systems of linear equations]]
see previous: [[Vectors]]
