*It is at this time that i decided to make my notes into a comprehensive textbook, so things before this are incomplete. My apologies to the reader.*
## Homogenous Systems
#homogenous_systems A system of linear equations is homogenous if the constant term in each equation is zero. If a system is not homogenous, we say its #inhomogenous . Homogenous systems always pass through the origin)
For example, 

$$
\begin{align}
x_{1}-7x_{2}+2x_{3}=0\\
-4x_{1} + x_{2}-x_{3}=0
\end{align}
$$
is a homogenous system. These equations form two planes that pass through the origin.

Homogenous systems always have at least one solution (the trivial solution, ie the $\vec{0}$). 
From the rank theorem: If a homogenous system has $m$ equations and $n$ variables, and $m<n$, then the system has $\infty$ many solutions.

## Linear combinations
given two vectors $\vec{a_{1}},\vec{a_{2}}$ how do we find if $\vec{b}$ is a linear combination of $a_{1}$ or $a_{2}$?
We can write a system of equations to solve, letting $x_{1}$ and $x_{2}$ be real numbers. 
$$
x_{1} a_{1} + x_{2}a_{2} \stackrel{?}{=} b $$
Geometrically, this corresponds to adding together some number of each vector to define a point. If the 2d vectors are on the same line they can't define $\mathbb{R}^{2}$, but if they don't align then they can.

#span
the span of a set of vectors produces a subset of $\mathbb{R}^{n}$ and is denoted span$\{ \vec{v}_{1},\vec{v}_{2},\dots,\vec{v}k \}$. if the vectors can produce $\mathbb{R}^{n}$ then they are called a #spanning_set for $\mathbb{R}^{n}$  
If a vector is a linear combination of other vectors, it won't increase the span. 

To calculate the span of a set, ie 
$$a = \begin{pmatrix}
1 \\ 2 \\ 3
\end{pmatrix},b=\begin{pmatrix}
1 \\
1 \\
-1
\end{pmatrix}
$$
We need to find $S_{1}\text{and}S_{2}$, solutions to find any x y z.
$$
s_{1}\begin{pmatrix}
1 \\
2 \\
3 
\end{pmatrix} + s_{2}\begin{pmatrix}
1 \\
1 \\
-1
\end{pmatrix} = \begin{pmatrix}
x \\
y \\
z
\end{pmatrix}
$$

We write the system as an augmented matrix
$$
\begin{bmatrix}
1 & 2 & | & x \\
2 & 1 & | & y \\
0 & -1 &| & z 
\end{bmatrix}
 = \begin{bmatrix}
1 & 1  & | & x\\
0 & 1 & | & 2x-y \\
0 & 0 & | & -2x+y-z
\end{bmatrix}$$
So$$
\text{Span}\left\{  \begin{pmatrix}
1 \\
2 \\
0
\end{pmatrix},\begin{pmatrix}
1 \\
1 \\
01
\end{pmatrix}  \right\} 
 = \left\{ \begin{pmatrix}
x \\
y \\
z
\end{pmatrix}:-2x+y-z = 0 \right\} $$
This gives us the entire plane that the two vectors can define. the 0 0 row is a constraint as it can't be in $\mathbb{R}^{3}$. We only have two vectors, so there can only be 2 leading variables. 
$-2x+y-z=0$ is the normal vector of the plane

Some more examples: 

$$
\begin{pmatrix}
1 & -2 & | & x \\
-1 & 2 & | & y \\
2 & -4 & | & z
\end{pmatrix} \to \begin{pmatrix}
1 & -2 & | & x \\
0 & 0 & | & x+y \\
0 & 0 & | & z-2x
\end{pmatrix}
$$

We get a line as the intersection of two planes. The span of this is a single line that follows the constraints. The two vectors are a multiple of each other (-2 in this case)

**If we add a new point that already satisfies the constraints given, it will not grow the span at all** 
IE if a new vector satisfies $z-2x = 0$ and $0=x+y$ then it maintains the current span. Otherwise, if it breaks the constraints it is giving us more information, and allows us one more dimension to span. 


## Linear independence
A set of vectors is #linearly_dependent if there are scalars $c_{1},c_{2},\dots ,c_{k}$ that are not all zero such that 
$$
c_{1}\vec{v}_{1}+c_{2}\vec{v}_{2}+\dots+c_{k}\vec{v}_{k} = 0
$$
A set of vectors that is not linearly independent, it is #linearly_indepent
This is a property of the entire set of vectors. 
We write the set of vectors in an augmented matrix with zero as last row. 

Theorem: The set v1-vm is linearly dependent if and only if the homogenous linear system with the augmented matrix of each vector | 0 has a nontrivial solution.

see next: [[Matrix operations]]
see previous: [[Systems of linear equations]]
