![[Pasted image 20240129191724.png]]
A) 

Because $w$ is a linear combination of vectors $u_{1},\dots,u_{k}$, , by definition there exist some set $(c_{1},c_{2}\dots c_{k})$ such that $\sum_{i=0}^{k}c_{i}u_{i}$ that generate $w$. Because $u_{k}$ is a linear combination, by definition there exists some set $p_{1},p_{2}\dots p_{m}$ such that $\sum_{j=0}^{m}p_{j}v_{j}$ = $u_{k}$. We can now rewrite the previous expression:  $$
w = \sum_{i=0}^{k}c_{i}u_{i} = \sum_{i=0}^{k}c_{i}\sum_{j=0}^{m}p_{j}v_{j}
$$
We have a maximum upper limit of the span given by vectors $u_{1}\dots u_{k}$
given by the span of $(v_{1},\dots,v_{m})$, as each we can define $u_{i}$ as $u_{i}=v_{i}$  for I $\in \left\{ 0,1,\dots \right\}$.
 
 If $k<m$, any remaining $u$ as the zero vector. Because there can't be a $U_{k}$ that isn't defined by some $V_{m}$, we know that the maximum span is $\text{Span}(v_{1},\dots,v_{m})$ .

 If $m < k$ than we know that the span must be $<$ $\text{Span}(v_{1},\dots,v_{m})$, as there are not enough vectors $U_{k}$ to match for each in $V_{m}$. This means that $\text{Span}(u_{1},\dots u_{k}) \subseteq(v_{1},\dots v_{m})$

B) For each $V_{j}$ to be given by the set of U's, and each $U_{k}$ to be a combination of the set of V's, the span of each can not be higher than the other. Because neither span may be higher than the other, both spans must equal.  

![[Pasted image 20240129195723.png]]
a) By definition, being linearly independent means that the $n\times n$ matrix can be turned to reduced row echelon form such that each column and row has only one 1, and all remaining spots as zero, with no columns or rows of all zero. 
$$
\begin{bmatrix}
1 & 0 & \dots  & \dots & 0 \\
0  & 1 & 0 & \dots & 0\\
\vdots  & \ddots & \ddots & \ddots & 0\\ 
\vdots  & \ddots &\ddots & 1 & 0\\
0  &  0 & 0 & \dots & 1
\end{bmatrix}
$$
This definition means that there is 1 leading variable per column, meaning that the $n\times n$ matrix has $n$ leading variables. Rank of a matrix is, by definition, the number of leading variables. Thus, the span of a linearly independent $n\times n$ matrix is $\mathbb{R}^{n}$.  Because the matrix is square, $\text{Rank}\left( n\times n \text{ matrix}\right) = \text{number of columns} = \text{number of rows} = n$

![[Pasted image 20240129201546.png]]



Prove that two vectors are linearly dependent if and only if one is a scalar multiple of the other.

By definition, vectors are linearly dependent if there exist some constants such that $$
\vec{v}_{1}c_{1} + \vec{v}_{2}c_{2} \dots + \vec{v}_{nc_{n}} = 0
$$Because we only have two vectors, this means that the two vectors are only dependent if
$$
\begin{align*}
\vec{v}_{1}c_{1}+\vec{v}_{2}c_{2} = 0 \implies \\
\vec{v}_{1}c_{1}=-\vec{v}_{2}c_{2} \implies \\
\vec{v}_{1} = -\frac{\vec{v}_{2}c_{2}}{c_{1}} \\
\end{align*}
$$ $\frac{-c2}{c1}$ is a constant, and can be written as k. Thus,
$\vec{v_{1}} = k \vec{v}_{2}$
This proves that two vectors that are the only vectors in a system are only linearly dependent if one is a multiple of the other.



let us assume that $v=c_{1}\vec{v}_{1}+\dots c_{k}\vec{v}_{k}$, where $c_{1},\dots,c_{k}$ are scalers in $\mathbb{R}^{n}$ with $c_{1}\neq 0$
Suppose the set $\{\vec{0}, v_{1},v_{2},\dots v_{k} \}$ is linearly dependent.  $\vec{0} = s_{1}\vec{v}_{1}+s_{2}\vec{v}_{2}+\dots+s_{k}\vec{v}_{k}$ where $s_{1} = 0$. 

Given that $v = c_{1}\vec{v}_{1} + \dots c_{k}\vec{v}_{k}$, $s_{1}c_{1}\vec{v}_{1}+(s_{1}c_{2}+s_{2})\vec{v}_{2} + \dots + (s_{1}c_{k}+s_{k})\vec{v}_{k}$ .
Given that $s_{1}=0$, this implies $s_{2}..s_{k}$ are also 0. This contradicts the definition of linear dependence, where at least one scalar must be nonzero, because the set of scalars $s_{1},\dots s_{k}$ - which form $\vec{0}$ - are all 0. Thus, $\{ v,v_{2},\dots,v_{k} \}$ is linearly independent.














Let $\{\mathbf{v}_1,...,\mathbf{v}_k\}$ be a linearly independent set of vectors in $\mathbb{R}^n$, and let $\mathbf{v}$ be a vector in $\mathbb{R}^n$.
Suppose that $\mathbf{v} = c_1\mathbf{v}_1 + c_2\mathbf{v}_2 + \cdots + c_k\mathbf{v_k}$ with $c_1 \neq 0$.
Prove that $\{\mathbf{v}, \mathbf{v}_2, \dots, \mathbf{v}_k\}$ is linearly independent.

The set of vectors $v,v_{1}\dots v_{k}$ must be linearly dependent, and the set of vectors of $v,v_{2}\dots v_{k}$ must be linearly independent. 

We can prove this by contradiction: 
If we assume, for the sake of contradiction, that $v,v_{2}\dots v_{k}$ is linearly dependent, then there must exist some constants $c_{2}\dots c_{k}$ such that v = $c_{2}v_{2}+\dots c_{k}v_{k}$. 

If this is true, then for the set of vectors $v = v_{2},\dots,v_{k}$ there exist the same set of constants to define v. Thus, for the set $v_{1},v_{2}\dots v_{k}$ the same constants can be used.  We can then say that $$
\begin{align}
v = kv_{1}+c_{2}v_{2}+\dots c_{n}v_{n} \\
v = kv_{1}+v \\
0 = kv_{1}
\end{align}
$$
For this statement to be true, $c_{1}$ must be zero. 

We are given that $v_{1}\dots v_{k}$ is linearly independent, so there do not exist other constants such that $v_{1}=c_{2}v_{2}+c_{3}v_{3}\dots c_{n}v_{n}$. Because $c_{1} \neq 0$, $v$ must be dependent on the set $v_{1}\dots v_{k}$ and independent on the set $v_{2}\dots v_{k}$. 

Because $v_{1},v_{2}\dots v_{k}$ is independent and $v,v_{1},v_{2}\dots v_{k}$ is dependent





















