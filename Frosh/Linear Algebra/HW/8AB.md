  Determine whether the set $\mathcal{B}$ is a basis for the vector space $V$, where
$$
V = M_{22}
\text{ \ and \ }
\mathcal{B} = \left\{
\begin{bmatrix*}[r] 1 & 0 \\ 0 & 1 \end{bmatrix*},
\begin{bmatrix*}[r] 0 & 1 \\ 1 & 0 \end{bmatrix*},
\begin{bmatrix*}[r] 1 & 1 \\ 0 & 1 \end{bmatrix*},
\begin{bmatrix*}[r] 1 & 0 \\ 1 & 1 \end{bmatrix*}
\right\}.

$$
We have two properties that we must uphold:
1) If B is a basis for $V$, then for every $\vec{v}\in V$, there is exactly one way to write $\vec{v}$ as a linear combination of the vectors in $B$. 
2) If $V$ has a basis with $n$ vectors, then every basis of $V$ has exactly $n$ vectors. Any fewer doesn't span $V$, any more is linearly dependent.

We can first check that $B$ is in the span of $V$, and that it holds linear independence.

$$
c_{1}\begin{bmatrix*}[r] 1 & 0 \\ 0 & 1 \end{bmatrix*}+
c_{2}\begin{bmatrix*}[r] 0 & 1 \\ 1 & 0 \end{bmatrix*}+c_{3}
\begin{bmatrix*}[r] 1 & 1 \\ 0 & 1 \end{bmatrix*}+
c_{4}\begin{bmatrix*}[r] 1 & 0 \\ 1 & 1 \end{bmatrix*} = \begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
$$
This yields the equations

$$
\begin{bmatrix}
1 & 0 & 1 & 1  \\
0 & 1 & 1 & 0 \\
0 & 1 & 0 & 1 \\
1 & 0 & 1 & 1
\end{bmatrix}
\begin{bmatrix}
c_{1}\\ c_{2}\\ c_{3}\\ c_{4}
\end{bmatrix} = \begin{bmatrix}
a \\ b \\ c \\ d
\end{bmatrix}
$$
We can row reduce this and find
$$
\begin{align}
R_{4}\to  R_{4}-R_{1},R_{3}\to  R_{3}-R_{2}\\
\begin{bmatrix}
1 & 0 & 1 & 1  \\
0 & 1 & 1 & 0 \\
0 & 0 & -1 & 1 \\
0 & 0 & 0 & 0
\end{bmatrix} \\
\end{align}
$$
$$
\begin{align}
R_{1}\to  R_{1}+R_{3},R_{2}\to  R_{2}+R_{2}\\
\begin{bmatrix}
1 & 0 & 0 & 2  \\
0 & 1 & 0 & 1 \\
0 & 0 & -1 & 1 \\
0 & 0 & 0 & 0
\end{bmatrix}  \\
R_{3}\to  -R_{3} \\
\begin{bmatrix}
1 & 0 & 0 & 2  \\
0 & 1 & 0 & 1 \\
0 & 0 & 1 & -1 \\
0 & 0 & 0 & 0
\end{bmatrix}  \\
\end{align}
$$
We can see that $\beta$ is not linearly independent, so it can not form a basis for $V$.




Find the coordinate vectors $[p(x)]_\mathcal{B}$ and $[p(x)]_\mathcal{C}$ of $p(x)$ with respect to the bases $\mathcal{B}$ and $\mathcal{C}$, respectively.
Find the change-of-basis matrix $P_{\mathcal{C} \leftarrow \mathcal{B}}$ from $\mathcal{B}$ to $\mathcal{C}$.
Use your answer to part (b) to compute $[p(x)]_\mathcal{C}$, and compare your answer with the one found in part (a).
Find the change-of-basis matrix $P_{\mathcal{B} \leftarrow \mathcal{C}}$ from $\mathcal{C}$ to $\mathcal{B}$.
Use your answers to parts (c) and (d) to compute $[p(x)]_\mathcal{B}$, and compare your answer with the one found in part (a).
$$
p(x) = 1 + 3x
        \text{ \ and \ }
        \mathcal{B} = \left\{ 1+x, 1-x \right\}
        \text{ \ and \ }
        \mathcal{C} = \left\{ 2x, 4 \right\} \ \ \text{in $\mathscr{P}_1$}
$$

A)
We can write p(x) in the standard basis as $\begin{bmatrix}1 & 0 \\ 0 &1\end{bmatrix}\begin{bmatrix}1 \\ 3\end{bmatrix}$. 

We can find the change of basis and transform p(x) between the standard basis and c by $$ 
\begin{bmatrix}
    \begin{bmatrix}
    1 \\ 0
\end{bmatrix}_c, \begin{bmatrix}
    0 \\ 1
\end{bmatrix}_c
\end{bmatrix}
\begin{bmatrix}
    1 \\ 3
\end{bmatrix}$$
To find the first vector, this is constants $c_{1}\text{ and } c_{2}$ that satisfy
$$
\begin{bmatrix}
1 \\ 0 
\end{bmatrix} =
c_{1} \begin{bmatrix}
0 \\ 2
\end{bmatrix} +c_{2} \begin{bmatrix} 4 \\ 0
\end{bmatrix}
$$
The solution is $$
\begin{bmatrix}
0 \\ \frac{1}{4}
\end{bmatrix}
$$
So this is the x coordinate transformed into $c$. 
We can do the same for the $\hat{y}$ vector and find that $\begin{bmatrix}0\\1\end{bmatrix}_{c}= \begin{bmatrix}\frac{1}{2}\\0 \end{bmatrix}$
Thus, 

$$
\begin{bmatrix}
1 \\ 3
\end{bmatrix}_{c} = \begin{bmatrix}
0 & \frac{1}{2} \\
\frac{1}{4} & 0
\end{bmatrix}_{c \leftarrow I} \begin{bmatrix}
1 \\ 3
\end{bmatrix}_{c} = \begin{bmatrix}
\frac{3}{2} \\
 \frac{1}{4}
\end{bmatrix}
$$


We can also find $\begin{bmatrix}1\\3\end{bmatrix}_{b}$ by the same process.
$$
\begin{bmatrix}
    \begin{bmatrix}
    1 \\ 0
\end{bmatrix}_b, \begin{bmatrix}
    0 \\ 1
\end{bmatrix}_b
\end{bmatrix}
\begin{bmatrix}
    1 \\ 3
\end{bmatrix}
$$
We can now find these two vectors:

 We can now find $\begin{bmatrix}1 \\ 0\end{bmatrix}_{b}$ as the coefficients in 

$$
\begin{bmatrix}
1 \\0
\end{bmatrix}_{b} = c_{1} \begin{bmatrix}
1 \\ 1
\end{bmatrix} + c_{2}\begin{bmatrix}
1 \\ -1
\end{bmatrix}
$$
We can write this as
$$
\begin{align}
\begin{bmatrix}
1 & 1 & | & 1 \\
1 & -1 & | & 0
\end{bmatrix} \rightarrow \begin{bmatrix}
2 & 0 & | & 1 \\
1 & -1 & | & 0
\end{bmatrix} \\
=\begin{bmatrix}
1 & 0 & | & \frac{1}{2} \\
0 & -1 & | & -\frac{1}{2}
\end{bmatrix}
\end{align}
$$
thus $c_{1}=c_{2}=\frac{1}{2}$. This means that 
$$
\begin{bmatrix}
1 \\0 
\end{bmatrix}_{b} = \begin{bmatrix}
\frac{1}{2} \\ \frac{1}{2}
\end{bmatrix}
$$


$$
\begin{bmatrix}
0 \\1
\end{bmatrix}_{b} = c_{1} \begin{bmatrix}
1 \\ 1
\end{bmatrix} + c_{2}\begin{bmatrix}
1 \\ -1
\end{bmatrix}
$$
We can rewrite this as a system of equations
$$
\begin{align}
\begin{bmatrix}
1 & 1 & | & 0 \\
1 & -1 & | & 1
\end{bmatrix} \\
\text{ this reduces to } \\
\begin{bmatrix}
2 & 0 & | & 1 \\
1 & -1 & | & 1
\end{bmatrix},
\end{align}
$$
Thus, $c_{1}=\frac{1}{2},c_{2}=-\frac{1}{2}$ 
So the $\begin{bmatrix}0\\1\end{bmatrix}_{b}=\begin{bmatrix} \frac{1}{2} \\ -\frac{1}{2}\end{bmatrix}$
This means that the vector 

$$
\begin{align}
\begin{bmatrix}
1 \\ 3
\end{bmatrix}_{b} = \begin{bmatrix}
\frac{1}{2}  & \frac{1}{2}\\ \frac{1}{2} & -\frac{1}{2}
\end{bmatrix} \begin{bmatrix}
1 \\ 3
\end{bmatrix} \\
= \begin{bmatrix}
\frac{1}{2}+\frac{3}{2} \\
\frac{1}{2} - \frac{3}{2}
\end{bmatrix} \\
\end{align}
$$
Thus, 
$$
\boxed{
\begin{bmatrix}
1 \\ 3
\end{bmatrix}_{b}= \begin{bmatrix}
2 \\ -1
\end{bmatrix}, \text{ and }  \begin{bmatrix}
1 \\\ 3\end{bmatrix}_{c} =\begin{bmatrix}
\frac{3}{2} \\
 \frac{1}{4}
\end{bmatrix}
}
$$

Find the change-of-basis matrix $P_{\mathcal{C} \leftarrow \mathcal{B}}$ from $\mathcal{B}$ to $\mathcal{C}$.
$$
p(x) = 1 + 3x
        \text{ \ and \ }
        \mathcal{B} = \left\{ 1+x, 1-x \right\}
        \text{ \ and \ }
        \mathcal{C} = \left\{ 2x, 4 \right\} \ \ \text{in $\mathscr{P}_1$}
$$
We can write $B$ as $\begin{bmatrix}1 & 1\\ 1 & -1\end{bmatrix}$ and $C$ as $\begin{bmatrix}0 & 4 \\ 2 & 0\end{bmatrix}$
We can find the change of basis from $B\rightarrow C$ by solving 
$$
\begin{bmatrix}
1 \\ 1
\end{bmatrix}_{c} = c_{1} \begin{bmatrix}
0 \\ 2
\end{bmatrix} + c_{2} \begin{bmatrix}
4 \\ 0
\end{bmatrix}
$$
$C_{1}=\frac{1}{2},c_{2}=\frac{1}{4}$
We must do the same for the other vector in $B$:
$$
\begin{bmatrix}
1 \\ -1
\end{bmatrix} = c_{1} \begin{bmatrix}
0 \\ 2
\end{bmatrix} + c_{2} \begin{bmatrix}
4 \\ 0
\end{bmatrix}
$$
so $c_{1} = -\frac{1}{2}, c_{2}=\frac{1}{4}$
Thus our change of basis matrix from $B\rightarrow C$ is
$$
\boxed{
\begin{bmatrix}
\frac{1}{2} & -\frac{1}{2} \\
\frac{1}{4} & \frac{1}{4}
\end{bmatrix}
}
$$

c) Use your answer to part (b) to compute $[p(x)]_\mathcal{C}$, and compare your answer with the one found in part (a).

Using $[p(x)]_{c}=\begin{bmatrix}1/2 & -1/2 \\ 1/4 & 1/4\end{bmatrix}_{c\leftarrow b}[p(x)]_{b}$
We can use the value from earlier:
$$
\begin{bmatrix}
1 \\ 3
\end{bmatrix}_{b}= \begin{bmatrix}
2 \\ -1
\end{bmatrix}
$$
Thus, 
$$
\boxed{
[p(x)]_{c} =\begin{bmatrix} \frac{1}{2} & \frac{-1}{2} \\ \frac{1}{4} & \frac{1}{4}\end{bmatrix}\begin{bmatrix}
2 \\ -1
\end{bmatrix} = \begin{bmatrix}
\frac{3}{2} \\
\frac{1}{4}
\end{bmatrix}
}
$$
This agrees with what we found previously. 


D) Find the change-of-basis matrix $P_{\mathcal{B} \leftarrow \mathcal{C}}$ from $\mathcal{C}$ to $\mathcal{B}$.

Recall:
$$
C = \begin{bmatrix}
0 & 4 \\
2 & 0
\end{bmatrix}, B= \begin{bmatrix}
1 & 1  \\
1 & -1
\end{bmatrix}
$$
To find the matrix $P_{b\leftarrow C}$ , we must  reduce $B$ to the identity and find the transformed $C$ (just learned this online)
$$
\begin{bmatrix}
1 & 1  & | & 0 & 4\\
1 & -1 & | & 2 & 0
\end{bmatrix}
$$
We can simplify this down
$$
\begin{align}
\begin{bmatrix}
1 & 1 & | & 0 & 4 \\
0 & -2 & | & 2 & -4
\end{bmatrix}\rightarrow \begin{bmatrix}
1 & 1 & | & 0 & 4 \\
0 & 1 & | & -1 & 2
\end{bmatrix}\rightarrow \\
\begin{bmatrix}
1 & 0 & | & 1 & 2 \\
0 & 1 & | & -1 & 2
\end{bmatrix}
\end{align}
$$
This is our change of basis matrix. 


E)  Use your answers to parts (c) and (d) to compute $[p(x)]_\mathcal{B}$, and compare your answer with the one found in part (a).
$$ 
[P(x)]_{c} = 
\begin{bmatrix}
\frac{3}{2} \\
\frac{1}{4}
\end{bmatrix}
$$

Using the change of basis matrix,
$$
\begin{align}
[P(x)]_{b} = \begin{bmatrix}
1 & 2 \\
-1 & 2
\end{bmatrix} \begin{bmatrix}
\frac{3}{2} \\ \frac{1}{4}
\end{bmatrix} = \begin{bmatrix}
\frac{3}{2}+\frac{2}{4} \\
-\frac{3}{2}+\frac{2}{4}
\end{bmatrix}
\\
= \begin{bmatrix}
2 \\
-1
\end{bmatrix}
\end{align}
$$
This agrees with the value we found in part $A$. 

We have found that going from the identity version of a vector to basis B is the same as that version of a vector in a basis C taken to basis B. We can compute change of basis matrices and they are self consistent when representing any sequence of transformations between bases. 




For the set $B = \{        \mathbf{v}_1,        \mathbf{v}_1 + \mathbf{v}_2,        \mathbf{v}_1 + \mathbf{v}_2 + \mathbf{v}_3,        \dots,        \mathbf{v}_1 + \dots + \mathbf{v}_n    \}$ to be a basis for a vector space $V$, $B$ must be linearly independent and have $n$  unique vectors. The latter follows from the former, given that we have $n$ entries in the set for $B$. 

 $\{        \mathbf{v}_1,        \mathbf{v}_2,       \mathbf{v}_3,        \dots,        \mathbf{v}_n    \}$ is a basis iif every vector in the set must be linearly independent. Thus, B is a basis iif the set of sums of linearly independent vectors where every sum has a unique set of vectors drawn from the set is linearly independent. 
 
let $\left\{ \vec{B}_{1},\vec{B}_{2} \right\}$ be a linearly independent set
 $\vec{B}_{1}\stackrel{?}{=}c(\vec{B}_{1}+\vec{B}_{2})$
 $\vec{B}_{1}\stackrel{?}{=}c\vec{B}_{1}+c\vec{B}_{2}$
 $\vec{B}_{1}(1-c)\stackrel{?}{=}\vec{B}_{2}$
 Because the set is linearly independent, we can not get the vector $B_{2}$ with a scalar multiple of $B_{1}$. For our proof, let $\vec{B}_{1} = B_{i}$ and $\vec{B}_{2}$ be $B_{i+1}$. 

Therefore, $\left\{ v_{1},v_{1}+v_{2} \right\}$ is linearly independent. Applying this to every combinations of elements in the set $B$ yields $\left\{ v_{1},v_{1}+v_{2}+v_{3},v_{1}+v_{2}+\dots+v_{n}\right\}$ is linearly independent. 
 



 Let $\mathcal{B}$ and $\mathcal{C}$ be bases for $\mathscr{P}_2$.
If $\mathcal{B} = \{x, 1+x, 1-x+x^2\}$ and the change-of-basis matrix from $\mathcal{B}$ to $\mathcal{C}$ is

$$
P_{\mathcal{C} \leftarrow \mathcal{B}} = \begin{bmatrix*}[r]
1 & 0 & 0 \\
0 & 2 & 1 \\
-1 & 1 & 1
\end{bmatrix*}
$$
find $\mathcal{C}$.

We can express $B$ as a matrix:
$$
B = \begin{bmatrix}
0 & 1 & 1 \\
1 & 1 & -1 \\
0 & 0 & 1
\end{bmatrix}\begin{bmatrix}
1 \\ x \\ x^{2}
\end{bmatrix}
$$

We can find $C$ as 
$$
\begin{align}
C = P_{c \leftarrow  B}B \\
C = \begin{bmatrix*}[r]
1 & 0 & 0 \\
0 & 2 & 1 \\
-1 & 1 & 1
\end{bmatrix*}\begin{bmatrix}
0 & 1 & 1 \\
1 & 1 & -1 \\
0 & 0 & 1
\end{bmatrix}\begin{bmatrix}
1 \\ x \\ x^{2}
\end{bmatrix}
\end{align}
$$
Using the outer product expansion representation, this becomes

$$
\begin{bmatrix}
0 & 1 & 1 \\
0 & 0 & 0 \\
0 & -1 & -1
\end{bmatrix}+\begin{bmatrix}
0 & 0 & 0 \\
2 & 2 & -2 \\
1 & 1 & -1 \\
\end{bmatrix} + \begin{bmatrix}
0 & 0 & 0 \\
0 & 0 & 1 \\
0 & 0 & 1
\end{bmatrix}
$$
$$
C = \begin{bmatrix}
0 & 1 & 1 \\
2 & 2 & -1 \\
1 & 0 & -1
\end{bmatrix}\begin{bmatrix}
1 \\ x \\ x^{2}
\end{bmatrix}
$$
$$
C = \left\{ 2x+x^{2},1+2x,1-x-x^{2} \right\}
$$



Find the coordinate vectors $[p(x)]_\mathcal{B}$ and $[p(x)]_\mathcal{C}$ of $p(x)$ with respect to the bases $\mathcal{B}$ and $\mathcal{C}$, respectively.

Find the change-of-basis matrix $P_{\mathcal{C} \leftarrow \mathcal{B}}$ from $\mathcal{B}$ to $\mathcal{C}$.

Use your answer to part (b) to compute $[p(x)]_\mathcal{C}$, and compare your answer with the one found in part (a).

Find the change-of-basis matrix $P_{\mathcal{B} \leftarrow \mathcal{C}}$ from $\mathcal{C}$ to $\mathcal{B}$.

Use your answers to parts (c) and (d) to compute $[p(x)]_\mathcal{B}$, and compare your answer with the one found in part (a).
$$
p(x) = 4 - 2x - x^2
\text{ \ and \ }
\mathcal{B} = \left\{ x, 1+x^2, x+x^2 \right\}
\text{ \ and \ }
\mathcal{C} = \left\{ 1, 1+x, x^2 \right\} \ \ \text{in $\mathscr{P}_2$}
$$
First, $B$ can be represented as
$$
\begin{bmatrix}
0 & 1 & 0 \\
1 & 0 & 1 \\
0 & 1 & 1
\end{bmatrix}
$$
C can be written
$$
\begin{bmatrix}
1 & 1 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix}
$$
and $P$ can be written
$$
\begin{bmatrix}
1 & 0 & 0\\0 & 1 & 0 \\0 & 0 & 1
\end{bmatrix}\begin{bmatrix}
4 \\ -2 \\-1
\end{bmatrix}
$$

The change of basis $P_{C\leftarrow I}$ can be found by matrix reduction:
$$
\begin{bmatrix}
1 & 1 & 0 & | & 1 & 0 & 0 \\
0 & 1 & 0 & | & 0 & 1 & 0 \\
0 & 0 & 1 & | & 0 & 0 & 1
\end{bmatrix}
$$
This reduces to 
$$
\begin{bmatrix}
1 & 0 & 0 & | & 1 & -1 & 0 \\
0 & 1 & 0 & | & 0 & 1 & 0 \\
0 & 0 & 1 & | & 0 & 0 & 1
\end{bmatrix}
$$
Thus our change of basis $P_{C\leftarrow I}=\begin{bmatrix}1&-1&0\\0&1&0\\0&0&1\end{bmatrix}$
We can now compute $[P(x)]_{C}$
$$
\begin{align}
P(x)_{C}=P_{C\leftarrow  I}[P(x)]_{I} \\
P(x)_{C} = P_{C\leftarrow I}=\begin{bmatrix}1&-1&0\\0&1&0\\0&0&1\end{bmatrix}\begin{bmatrix}
4 \\ -2 \\-1
\end{bmatrix} \\
\end{align}
$$
Thus,
$$
\boxed{
P(x)_{C}=\begin{bmatrix}
4 & 2 & 0 \\
0 & -2 & 0 \\
0 & 0 & -1
\end{bmatrix}
}
$$


Similarly, we can find the change of basis $P_{B\leftarrow I}$
$$
\begin{align}
\begin{bmatrix}
0 & 1 & 0  & | & 1 & 0 & 0\\
1 & 0 & 1  & | & 0 & 1 & 0\\
0 & 1 & 1  & | & 0 & 0 & 1\\
\end{bmatrix} \\
\rightarrow \begin{bmatrix}
0 & 1 & 0  & | & 1 & 0 & 0\\
1 & 0 & 0  & | & 0 & 1 & -1\\
0 & 0 & 1  & | & 0 & 0 & 1\\
\end{bmatrix}  \\
\rightarrow \begin{bmatrix} 
1 & 0 & 0  & | & 0 & 1 & -1\\
0 & 1 & 0  & | & 1 & 0 & 0\\
0 & 0 & 1  & | & 0 & 0 & 1\\
\end{bmatrix}  \\
\end{align}
$$
Thus the change of basis matrix $P_{B\leftarrow I}=\begin{bmatrix}0&1&-1\\1&0&0\\0&0&1\end{bmatrix}$

Thus, $$
\begin{align}
[P(x)]_{B}= P_{B\leftarrow I} = \begin{bmatrix} 
0&1&-1\\1&0&0\\0&0&1\end{bmatrix}\begin{bmatrix}
4\\-2\\-1
\end{bmatrix} \\
\end{align}
$$
$$
\boxed{
[P(x)]_{B} = \begin{bmatrix}
0  & -2 & 1 \\
4 & 0 & 0 \\
0 & 0 & -1
\end{bmatrix}
}
$$

We can now find the change of basis between $B \text{ and } C, P_{C\leftarrow B}$
$$
\begin{align}
\begin{bmatrix}
1 & 1 & 0  & | & 0 & 1 & 0 \\
0 & 1 & 0 & | & 1 & 0 & 1 \\
0 & 0 & 1 & | & 0 & 1 & 1
\end{bmatrix} \\
\begin{bmatrix}
1 & 0 & 0  & | & -1 & 1 & -1 \\
0 & 1 & 0 & | & 1 & 0 & 1 \\
0 & 0 & 1 & | & 0 & 1 & 1
\end{bmatrix} \\
\end{align}
$$
Thus,
$$
\boxed{
P_{C\leftarrow  B}=\begin{bmatrix}
-1 & 1 & -1 \\
1 & 0 & 1 \\
0 & 1 & 1
\end{bmatrix}
}
$$
We can take $[P(x)]_{C}=P_{C\leftarrow B}[P(x)]_{B}$ using the previous answer and check:

$$
[P(x)]_{C}=\begin{bmatrix}
-1 & 1 & -1 \\
1 & 0 & 1 \\
0 & 1 & 1
\end{bmatrix} \begin{bmatrix}
0  & -2 & 1 \\
4 & 0 & 0 \\
0 & 0 & -1
\end{bmatrix}
$$

Using outer product expansion, 
$$
P(x)_{c} = \begin{bmatrix}
0  & 2 & 1 \\
0 & -2 & 1 \\
0 & 0 & 0
\end{bmatrix}+\begin{bmatrix}
4 & 0 & 0 \\
0 & 0 & 0 \\
4 & 0 & 0
\end{bmatrix}+\begin{bmatrix}
0 & 0 & 1 \\
0 & 0 & -1 \\
0 & 0 & -1
\end{bmatrix}
$$
$$
\boxed{
[P(x)]_{c} = \begin{bmatrix}
4 & 2 & 2 \\
0 & -2 & 0 \\
4 & 0 & -1
\end{bmatrix}
}
$$
$$
\boxed{
P(x)_{C}=\begin{bmatrix}
4 & 2 & 0 \\
0 & -2 & 0 \\
0 & 0 & -1
\end{bmatrix}
}
$$

