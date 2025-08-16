Let $V$ be a vector space with subspaces $U$ and $W$.
Define the \textbf{sum of $U$ and $W$} to be
$$
 U + W = \{\mathbf{u} + \mathbf{w} : \mathbf{u} \in U, \mathbf{w} \in W\}
$$
If $V = \mathbb{R}^3$, $U$ is the x-axis, and $W$ is the y-axis, what is $U + W$?
If $U$ and $W$ are subspaces of a vector space $V$, prove that $U + W$ is a subspace of $V$.

A)

Because we add elements component wise between $W$ and $U$, 
$W+U = \sum_{i=0}^{n}w_{i}+u_{i}$ 
We can see easily that for the integer elements, this is
$$
\begin{align}
c_{1}W+c_{2}U = c_{1} \begin{bmatrix}
1 \\ 0 \\ 0
\end{bmatrix} + c_{2} \begin{bmatrix}
0 \\ 1 \\ 0
\end{bmatrix}\\=
c_{1}\hat{X}+c_{2}\hat{Y} \,\, \, \forall \, c_{1},c_{2} \in \mathrm{Re}
\end{align}
$$

For $c_{1},c_{2}=(1,1)$, $W+U = \hat{X}+\hat{Y} = \begin{bmatrix}1\\1\\0\end{bmatrix}$

B)
By definition, for the set $V$ to be a vector space it must follow 10 axioms. Among those is the requirement that $V$ is closed under addition, ie $\vec{u}+\vec{v} \in V$.

For $V$ to be a vector space with $U \text{ and } W$ as subspaces, $U+W \in V$.

We saw earlier that the set defined by $\left\{ U,W \right\}$ is $c_{1}\hat{X}+c_{2}\hat{Y} \, \forall \, c_{1},c_{2} \in\mathrm{Re}$.
Because $0$ as a constant for $\hat{X},\hat{Y},\hat{Z}$ still maintains the vector in $\mathbb{R}^{3}$ ** , so $U+W \in \mathbb{R}^{3} \implies U+W\in V \forall c_{1},c_{2} \in \mathrm{Re}$  


** $\begin{bmatrix}0\\0\\0\end{bmatrix}\in\mathbb{R}^{3}$ 












We must show that the set $V$ is closed under addition and multiplication. 


Note that  $span(\vec{u}+\vec{w}) \in span(u)+span(w)$.
We know that $\hat{x} \in V \text{ and } \hat{y}\in V,$
Thus $(U+W)\in span(U)+span(W) \in span(V)$
So $U+W$ is a subset of $V$.



Is $M_{22}$ spanned by 
$$
	\begin{bmatrix*}[r] 1 & 0 \\ 1 & 0 \end{bmatrix*},
	\begin{bmatrix*}[r] 1 & 1 \\ 1 & 0 \end{bmatrix*},
	\begin{bmatrix*}[r] 1 & 1 \\ 1 & 1 \end{bmatrix*},
	\begin{bmatrix*}[r] 0 & -1\\ 1 & 0 \end{bmatrix*}
$$
?

To prove that this set spans $M_{2,2},$ we must see that we can generate every possible $2\times 2$ matrix with linear combinations of this set. That is, there exists constants $c_{1}\dots c_{4}$  such that
$$
A = 
c_{1} \begin{bmatrix}
1 & 0 \\ 1 & 0
\end{bmatrix} + c_{2} \begin{bmatrix}
1 & 1 \\ 1 & 0
\end{bmatrix} + c_{3} \begin{bmatrix}
1 & 1 \\ 1 & 1
\end{bmatrix} + c_{4} \begin{bmatrix}
0 & -1 \\ 1 & 0
\end{bmatrix}
$$
has a solution for every $A$. 


With the component wise definition of addition, this becomes
$$
\begin{align}
A = \begin{bmatrix}
c_{1}+c_{2}+c_{3} & c_{2}+c_{3}-c_{4} \\
c_{1}+c_{2}+c_{3}+c_{4} & c_{3} 
\end{bmatrix}
\end{align}
$$
With four free variables we can define any four combinations of numbers to fill each entry in the matrix, so this set of matrixes does span $M_{2,2}$






To do this, I will row reduce every matrix. We get

$$
\begin{bmatrix}
1 & 0 \\ 0 & 0
\end{bmatrix}, \begin{bmatrix}
0 & 1 \\
1 & 0
\end{bmatrix}, \begin{bmatrix}
1 & 1 \\
0 & 0
\end{bmatrix}, \begin{bmatrix}
0 & 0 \\ 1 & 1
\end{bmatrix}, \begin{bmatrix}
0 & 1 \\
1 & 0
\end{bmatrix}
$$
(there are two copies of one matrix with the values on the top or bottom). 
We can get rid of duplicates. This becomes

$$
\begin{bmatrix}
1 & 0 \\
0 & 0
\end{bmatrix},\begin{bmatrix}
0 & 1 \\
1 & 0 \\
\end{bmatrix}, \begin{bmatrix}
1 & 1 \\ 0 & 0
\end{bmatrix}, \begin{bmatrix}

\end{bmatrix}
$$
