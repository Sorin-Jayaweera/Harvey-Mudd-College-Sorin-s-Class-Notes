2.2.28:
First for simplicity, lets write the system in augmented matrix form:
$$\begin{bmatrix}
    2&3&-1&4 &| 1\\
    3&-1&0&1&|1\\
    3&-4&1&-1&|2\\
\end{bmatrix}$$
$R_{3} \leftrightarrow R_{2}$ 
$$\begin{bmatrix}
    2&3&-1&4 &| 1\\
    3&-4&1&-1&|2\\
    3&-1&0&1&|1\\
\end{bmatrix}$$

$R_{2}\to R_{2}+R_{1} - R_{3}$  
$$
\begin{bmatrix}
    2&3&-1&4 &| 1\\
    2&0&0&2&|2\\
    3&-1&0&1&|1\\
\end{bmatrix}
$$

$R_{1} \to R_{1}-R_{2}$ 
$$
\begin{align}
\begin{bmatrix}
0 & 3 & -1 & 2| & -1 \\
2 & 0 & 0 & 2 & | & 2 \\
3 & -1 & 0 & 1 & | & 1
\end{bmatrix}
\end{align}
$$
$R_{2}\leftrightarrow R_{1}$
$$
\begin{align}
\begin{bmatrix}
2 & 0 & 0 & 2 & | & 2 \\
0 & 3 & -1 & 2| & -1 \\
3 & -1 & 0 & 1 & | & 1
\end{bmatrix}
\end{align}
$$
$R_{1}\to\frac{R_{1}}{2}$
$$
\begin{align}
\begin{bmatrix}
1 & 0 & 0 & 1 & | & 1 \\
0 & 3 & -1 & 2| & -1 \\
3 & -1 & 0 & 1 & | & 1
\end{bmatrix}
\end{align}
$$
$R_{3}\to R_{3}-3R_{1}$
$$
\begin{align}
\begin{bmatrix}
1 & 0 & 0 & 1 & | & 1 \\
0 & 3 & -1 & 2| & -1 \\
0 & -1 & 0 & -2 & | & -2
\end{bmatrix}
\end{align}
$$
$R_{2} \to R_{2}+2R_{1}$
$$
\begin{align}
\begin{bmatrix}
1 & 0 & 0 & 1 & | & 1 \\
0 & 1 & -1 & -2 &| & -5 \\
0 & -1 & 0 & -2 & | & -2
\end{bmatrix}
\end{align}
$$
$R_{3} \to R_{3}+R_{2}$
$$
\begin{align}
\begin{bmatrix}
1 & 0 & 0 & 1 & | & 1 \\
0 & 1 & -1 & -2 &| & -5 \\
0 & 0 & -1 & -4 & | & -7
\end{bmatrix}
\end{align}
$$
$R_{3}\to -R_{3}$
$$
\begin{align}
\begin{bmatrix}
1 & 0 & 0 & 1 & | & 1 \\
0 & 1 & -1 & -2 &| & -5 \\
0 & 0 & 1 & 4 & | & 7
\end{bmatrix}
\end{align}
$$
$R_{2}\to R_{2}+R_{3}$
$$
\begin{align}
\begin{bmatrix}
1 & 0 & 0 & 1 & | & 1 \\
0 & 1 & 0 & 2 &| & 2 \\
0 & 0 & 1 & 4 & | & 7
\end{bmatrix}
\end{align}
$$
This is reduced Echelon form.
We can now solve the system of equations,
$$
\begin{align}
x_{1}+x_{4}=1 \\
x_{2}+2x_{4}=2 \\
x_{3}+4x_{4}=7 \\
\end{align}
$$
Which we can now solve.
$$
\begin{align}
x_{4} &= 1-x_{4} \\
&= 1-\frac{x_{2}}{2} \\
&= \frac{7}{4}-\frac{x_{3}}{4}
\end{align}
$$


2.2.30

Solve the following system of equations using either Gaussian or Gauss--Jordan elimination:$$

    \begin{bmatrix}
        -x_1 &+& 3x_2 &-& 2x_3 &+& 4x_4 &=& 0 \\
        2x_1 &-& 6x_2 &+& x_3 &-& 2x_4 &=& -3 \\
        x_1 &-& 3x_2 &+& 4x_3 &-& 8x_4 &=& 2
    \end{bmatrix}

$$

First, we can express this in augmented matrix form
$$
\begin{bmatrix}
-1 & 3 & -2 & 4 &|& 0 \\
2 & -6 & 1 & -2 &|&-3 \\
1 & -3 & 4 & -8 &|&2\\
\end{bmatrix}
$$
we can now begin simplifying with elementary row operations.
$$
\begin{align} \\
R_{1}\to R_{1}+R_{3} \\

\begin{bmatrix}
0 & 0 & 2 & -4 & | &2 \\
2 & -6 & 1 & -2 &|&-3 \\
1 & -3 & 4 & -8 &|&2\\
\end{bmatrix}
\end{align}
$$
We can rewrite this nicely with
$R_{1}\leftrightarrow R_{2}$
$$
\begin{bmatrix}
2 & -6 & 1 & -2 &|&-3 \\
0 & 0 & 2 & -4 & | &2 \\
1 & -3 & 4 & -8 &|&2\\
\end{bmatrix}
$$
and then doing $R_{1}\to R_{1}-R_{3}$
$$
\begin{bmatrix}
1 & -3 & -3 & 6 &|&-5 \\
0 & 0 & 2 & -4 & | &2 \\
1 & -3 & 4 & -8 &|&2\\
\end{bmatrix}
$$
and now $R_{3}\to R_{3}-R_{1}$
$$
\begin{bmatrix}
1 & -3 & -3 & 6 &|&-5 \\
0 & 0 & 2 & -4 & | &2 \\
0 & 0 & 1 & -14 &|&7\\
\end{bmatrix}
$$
then, $R_{1}\to R_{1}+3R_{3}$
$$
\begin{bmatrix}
1 & -3 & 0 & -36 &|&16 \\
0 & 0 & 2 & -4 &|&2 \\
0 & 0 & 1 & -14 &|&7\\
\end{bmatrix}
$$
and $R_{2}\to R_{2}-2R_{3}$
$$
\begin{bmatrix}
1 & -3 & 0 & -36 &|&16 \\
0 & 0 & 0 & -32 &|&-12 \\
0 & 0 & 1 & -14 &|&7\\
\end{bmatrix}
$$
and simplifying the middle row with $R_{2}\to \frac{R_{2}}{2}$
$$
\begin{bmatrix}
1 & -3 & 0 & -36 &|&16 \\
0 & 0 & 0 & -16 &|&-6 \\
0 & 0 & 1 & -14 &|&7\\
\end{bmatrix}
$$
we can now solve.
$$
\begin{align}
-16x_{4} = -6 &\implies x_{4} = \frac{6}{16} \\
x_{3} -\frac{14*6}{16} = 7 &\implies x_{3} = 21 \\
x_{1}-3x_{2} +13.5 = 16 &\implies \, \, x_{1}-3x_{2} = 2.5\\
\end{align}
$$



2.2.34
$$

    \begin{matrix*}[r]
        a &+& b &+& c &+& d &=& 4 \\
        a &+& 2b &+& 3c &+& 4d &=& 10 \\
        a &+& 3b &+& 6c &+& 10d &=& 20 \\
        a &+& 4b &+& 10c &+& 20d &=& 35
    \end{matrix*}

$$We can begin by writing this in augmented matrix form
$$
\begin{bmatrix}
1 & 1 & 1 & 1 & | & 4 \\
1 & 2 & 3 & 4 & | & 10 \\
1 & 3 & 6 & 10 & | & 20 \\
1 & 4 & 10 & 20 &| & 35 \\
\end{bmatrix}
$$
To begin, we can set each row $R_{n} \forall \{ N>1 \} = R_{n} - R_{1}$
$$
\begin{bmatrix}
1 & 1 & 1 & 1 & | & 4 \\
0 & 1 & 2 & 3 & | & 9 \\
0 & 2 & 5 & 9 & | & 19 \\
0 & 3 & 9 & 19 &| & 34 \\
\end{bmatrix}
$$
Now, we can subtract $R_{n} - R_{n,2}\times R_{2} \,\forall n\neq 2$ for every row
(Is this the correct math notation? I want to subtract the ith element of each row * R_2 for each row/column)
$$
\begin{bmatrix}
1 & 0 & -2 & -2 & | & -5 \\
0 & 1 & 2 & 3 & | & 9 \\
0 & 0 & 1 & 3 & | & 1 \\
0 & 0 & 3 & 10 &| & 7 \\
\end{bmatrix}
$$
Now we can do the same $R_{n} - R_{n,3}\times R_{3} \forall N\neq 3$
$$
\begin{bmatrix}
1 & 0 & 0 & 4 & | & -3 \\
0 & 1 & 0 & -3 & | & 6 \\
0 & 0 & 1 & 3 & | & 1 \\
0 & 0 & 0 & 1 &| & 4 \\
\end{bmatrix}
$$
and the same for the fourth column:  $R_{n} - R_{n,4}\times R_{4} \forall N\neq 4$
$$
\begin{bmatrix}
1 & 0 & 0 & 0 & | & 13 \\
0 & 1 & 0 & 0 & | & 18 \\
0 & 0 & 1 & 0 & | & -11 \\
0 & 0 & 0 & 1 &| & 4 \\
\end{bmatrix}
$$
This yields the solution
$$
\begin{align}
x_{1}&=13 \\
x_{2}&=18 \\
x_{3}&=-11 \\
x_{4}&=4
\end{align}
$$

We can take k = -1 and find:
$$
\begin{align}
\begin{matrix*}[r]
        -1x &+& 2y &=& 3 \\
        2x &-& 4y &=& -6
    \end{matrix*}\\
R_{1}\times 2 \implies \\
\begin{matrix*}[r]
        -2x &+& 4y &=& 6 \\
        2x &-& 4y &=& -6
\end{matrix*}\\
\implies \\
0 = 0, \text{which is true for all x y}
\end{align}
$$
If we take k = 1, we find
$$
\begin{align}
\begin{matrix*}[r]
     1x &+& 2y &=& 3 \\
        2x &-& 4y &=& -6
    \end{matrix*}\\
R_{1}\times 2 \implies \\
\begin{matrix*}[r]
        2x &+& 4y &=& 6 \\
        2x &-& 4y &=& -6
\end{matrix*}\\
\implies  \\
4x = 0, x = 0,y = \frac{6}{4}\\
0 = 0, \text{which is true for all x y}
\end{align}
$$


For what value(s) of $k$, if any, will the following system have (a) no solution, (b) a unique solution, and (c) infinitely many solutions?

$$
\begin{matrix*}[r]
  x &-& 2y &+& 3z &=& 2 \\
  x &+& y &+& z &=& k \\
  2x &-& y &+& 4z &=& k^2
\end{matrix*}
$$





First, lets write this in augmented matrix form:
$$
\begin{bmatrix}
1 & -2 & 3 & | & 2 \\
1 & 1 & 1 & | & k \\
2 & -1 & 4 & | & k^{2}
\end{bmatrix}
$$
we can use elementary row operations to solve this
set $R_{2} \to R_{2}-R_{1}$ and $R_{3} \to R_{3}-2R_{1}$
$$
\begin{bmatrix}
1 & -2 & 3 & | & 2 \\
0 & -1 & -1 & | & k-2 \\
0 & 3 & -2 & | & k^{2}-4
\end{bmatrix}
$$
now we can set $R_{2}\to -R_{2}$
$$
\begin{bmatrix}
1 & -2 & 3 & | & 2 \\
0 & 1 & 1 & | & -k+2 \\
0 & 3 & -2 & | & k^{2}-4
\end{bmatrix}
$$
next, $R_{1} \to R_{1}+2R_{2}$
$$
\begin{bmatrix}
1 & 0 & 5 & | & 2 -2k +4 \\
0 & 1 & 1 & | & -k+2 \\
0 & 3 & -2 & | & k^{2}-4
\end{bmatrix}
$$
$R_{3} \to R_{3}-3R_{2}$
$$
\begin{bmatrix}
1 & 0 & 5 & | & 2 -2k +4 \\
0 & 1 & 1 & | & -k+2 \\
0 & 0 & -5 & | & k^{2}-4+3k-6
\end{bmatrix}
$$
$R_{1} \to R_{1}+R_{3}$
$$
\begin{bmatrix}
1 & 0 & 0 & | & -4 +k + k^{2} \\
0 & 1 & 1 & | & -k+2 \\
0 & 0 & -5 & | & k^{2}-4+3k-6
\end{bmatrix}
$$
$R_{3}\to \frac{R_{3}}{-5}$
$$
\begin{bmatrix}
1 & 0 & 0 & | & -4 +k + k^{2} \\
0 & 1 & 1 & | & -k+2 \\
0 & 0 & 1 & | & \frac{k^{2}-4+3k-6}{-5}
\end{bmatrix}
$$
and finally $R_{2}\to R_{2}-R_{3}$
$$
\begin{bmatrix}
1 & 0 & 0 & | & -4 +k + k^{2} \\
0 & 1 & 0 & | & \frac{5k-10}{-5} - \frac{k^{2}-4+3k-6}{-5} \\
0 & 0 & 1 & | & \frac{k^{2}-4+3k-6}{-5}
\end{bmatrix} = 
\begin{bmatrix}
1 & 0 & 0 & | & -4 +k + k^{2} \\
0 & 1 & 0 & | & \frac{-2k+k^2}{5} \\
0 & 0 & 1 & | & \frac{k^{2}-4+3k-6}{-5}
\end{bmatrix} = 
$$
This means, $x_{1} = -4 +k + k^{2} , x_{2} =\frac{-2k+k^{2}}{5},x_{3} = \frac{k^{2}-4+3k-6}{-5}$






$$
\begin{bmatrix}
x &-& 2y &+& 3z &=& 2 \\
x &+& y &+& z &=& k \\
2x &-& y &+& 4z &=& k^2
\end{bmatrix}
$$
$R_{3}\to -R_{3}$  
$$
\begin{bmatrix}
1 &-& 2 &+& 3 &=& 2 \\
1 &+& 1 &+& 1 &=& k \\
-2 &+& 1 &-& 4 &=& -k^2
\end{bmatrix}
$$
$R_{3}\to R_{3}+R_{2}+R_{1}$ 
  $$
\begin{bmatrix}
1 &-& 2 &+& 3 &=& 2 \\
1 &+& 1 &+& 1 &=& k \\
0 &+& 0 &-& 0 &=& -k^2+k+2
\end{bmatrix}
$$
This implies that $K^2-k-2 = 0$ 
this yields k = -1 or k = 2.
Any other value yields no solution.


Show that $$
\mathbb{R}^2 = \textnormal{span}\left( \begin{bmatrix*}[r] 3 \\ -2 \end{bmatrix*}, \begin{bmatrix*}[r] 0 \\ 1 \end{bmatrix*} \right)$.

$$
we can check the rank of the matrix. 
Lets set these up nicely:
$$
\begin{bmatrix}
3 & 0 \\
-2  & 1
\end{bmatrix}
$$
we can multiply $R_{1} \to \frac{R_{1}}{3}$ which yields 
$$
\begin{bmatrix}
1 & 0 \\
-2 & 1
\end{bmatrix}
$$
we can now perform $R_{2} \to R_{2}+2R_{1}$
which yields
$$
\begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix}
$$
We can see easily that these are two basis vectors that are perpinidicular to each other, and are the general definition of $\mathbb{R}^2$


Show tha
t $\mathbb{R}^3 = \textnormal{span}\left( \begin{bmatrix*}[r]1 \\ 1 \\ 0\end{bmatrix*}, \begin{bmatrix*}[r] 1 \\ 2 \\ 3 \end{bmatrix*}, \begin{bmatrix*}[r] 2 \\ 1 \\ -1 \end{bmatrix*} \right)$.

First, lets make this look nicer:
$$
\begin{bmatrix}
1 & 1 & 2 \\
1 & 2 & 1 \\
0 & 3 & -1
\end{bmatrix}
$$
we can now simplify the matrix.
$R_{2}\to R_{2}-R_{1}$
$$
\begin{bmatrix}
1 & 1 & 2 \\
0 & 1 & -1 \\
0 & 3 & -1
\end{bmatrix}
$$
$R_{1}\to R_{1}-R_{2}$
$$
\begin{bmatrix}
1 & 0 & 3 \\
0 & 1 & -1 \\
0 & 3 & -1
\end{bmatrix}
$$
$R_{3}\to R_{3}-3R_{2}$
$$
\begin{bmatrix}
1 & 0 & 3 \\
0 & 1 & -1 \\
0 & 0 & 2
\end{bmatrix}
$$
$R_{3}\to \frac{R_{3}}{2}$
$$
\begin{bmatrix}
1 & 0 & 3 \\
0 & 1 & -1 \\
0 & 0 & 1
\end{bmatrix}
$$
$R_{2}\to R_{2}+R_{3}$ and $R_{1}\to R_{1}-3R_{3}$
$$
\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix}
$$
we can see that this is the unit vector matrix that defines $\mathbb{R}^3$, so the span of the three vectors is $\mathbb{R}^3$





Determine if the vector $\mathbf{b}$ is in the span of the columns of the matrix $A$ where
$$
A = \begin{bmatrix*}[r]
        1 & 2 & 3 \\
        5 & 6 & 7 \\
        9 & 10 & 11
    \end{bmatrix*}
    \textnormal{ \ \ and \ \ }
    \mathbf{b} = \begin{bmatrix*}[r]
        4 \\ 8 \\ 12
    \end{bmatrix*}. 
$$ 


We must find a vector $\vec{x}$ such that A$\vec{x} = B$.
We can write this in augmented matrix form to find X. If there is no solution, than B is not in the span of A. 
$$
\begin{bmatrix}
1 & 2 & 3 & | & 4 \\
5 & 6 & 7 & | & 8 \\
9 & 10 & 11 & | & 12 \\
\end{bmatrix} \begin{align}
\xrightarrow {R_{2}\to R_{2}-5R_{1}} \\
\xrightarrow {R_{3}\to R_{3}-9R_{1}}
\end{align}
\begin{bmatrix}
1 & 2 & 3 & | & 4 \\
0 & -4 & -8 & | & -12 \\
0 & -8 & -16 & | & -24 \\
\end{bmatrix}
$$
$$
\begin{align}
\xrightarrow {x_{2}\to \frac{x_{2}}{-4}} \\
\xrightarrow {x_{3}\to \frac{x_{3}}{-8}}
\end{align}
\begin{bmatrix}
1 & 2 & 3 & | & 4 \\
0 & 1 & 2 & | & 3 \\
0 & 1 & 2 & | & 3
\end{bmatrix}
\xrightarrow {\begin{align}
x_{1}\to x_{1}-2x_{2} \\
x_{3}\to x_{3}-x_{2}
\end{align}}
\begin{bmatrix}
1 & 0 & -1 & | & -2 \\
0 & 1 & 2 & | & 3 \\
0 & 0 &0 & | & 0
\end{bmatrix}
$$

$$
\vec{x}A = B
$$











$$\begin{pmatrix}
    w\\x\\y\\
\end{pmatrix} = \begin{pmatrix}
    1-s\\2-2s\\7-4s\\
\end{pmatrix}
= \{ s \begin{pmatrix}
    -1\\-2\\-4
\end{pmatrix} + \begin{pmatrix}
    1\\2\\7
\end{pmatrix} : s \in \mathbb{R}^{} \}$$




ONES TO CORRECT:
2.2.30

$$
    \begin{bmatrix}
        -x_1 &+& 3x_2 &-& 2x_3 &+& 4x_4 &=& 0 \\
        2x_1 &-& 6x_2 &+& x_3 &-& 2x_4 &=& -3 \\
        x_1 &-& 3x_2 &+& 4x_3 &-& 8x_4 &=& 2
    \end{bmatrix}
$$
First lets represent this as an augmented matrix
$$
\begin{bmatrix}
-1 & 3 & -2 & 4 & | & 0 \\
2 & -6 & 1 & -2 & | & -3 \\
1 & -3 & 4 & -8 & | & 2 \\
\end{bmatrix}
$$
We can rearrange this and simplify each row
$R_{1}\leftrightarrow R_{3}$
$$
\begin{bmatrix}
1 & -3 & 4 & -8 & | & 2 \\
2 & -6 & 1 & -2 & | & -3 \\
-1 & 3 & -2 & 4 & | & 0 \\
\end{bmatrix}
$$

$$
\xrightarrow {
\begin{align}
R_{3}\to R_{3}+R_{1} \\ 
R_{2}\to R_{2}-2R_{1}
\end{align}} \\
\begin{bmatrix}
1 & -3 & 4 & -8 & | & 2 \\
0 & 0 & -7 & 14 & | & -7 \\
0 & 0 & 2 & -4 & | & 2 \\
\end{bmatrix}
\xrightarrow {R_{3}\leftrightarrow R_{2}}
\begin{bmatrix}
1 & -3 & 4 & -8 & | & 2 \\
0 & 0 & 2 & -4 & | & 2 \\
0 & 0 & -7 & 14 & | & -7 \\
\end{bmatrix}
$$
$$
\xrightarrow {R_{2}\to \frac{R_{2}}{2}}
\begin{bmatrix}
1 & -3 & 4 & -8 & | & 2 \\
0 & 0 & 1 & -2 & | & 1 \\
0 & 0 & -7 & 14 & | & -7 \\
\end{bmatrix}
\xrightarrow {\begin{align}
R_{3}\to R_{3}+7R_{2} \\
R_{1}\to R_{1}-4R_{2}
\end{align}}
\begin{bmatrix}
1 & -3 & 0 & 0 & | & -2 \\
0 & 0 & 1 & -2 & | & 1 \\
0 & 0 & 0 & 0 & | & 0 \\
\end{bmatrix}
$$

We can now see the solution.
$$\begin{align}
x_{1}-3x_{2}=-2 \\
x_{3}-2x_{4}=1
\end{align}$$






Determine if the vector $\mathbf{b}$ is in the span of the columns of the matrix $A$ where
$$
    A = \begin{bmatrix*}[r]
        1 & 2 & 3 \\
        5 & 6 & 7 \\
        9 & 10 & 11
    \end{bmatrix*}
    \textnormal{ \ \ and \ \ }
    \mathbf{b} = \begin{bmatrix*}[r]
        4 \\ 8 \\ 12
    \end{bmatrix*}. 
$$

We must find a vector $\vec{x}$ such that A$\vec{x} = B$.
We can write this in augmented matrix form to find $\vec{x}$. If there is no solution, than B is not in the span of A. 
$$
\begin{bmatrix}
1 & 2 & 3 & | & 4 \\
5 & 6 & 7 & | & 8 \\
9 & 10 & 11 & | & 12 \\
\end{bmatrix} \begin{align}
\xrightarrow {R_{2}\to R_{2}-5R_{1}} \\
\xrightarrow {R_{3}\to R_{3}-9R_{1}}
\end{align}
\begin{bmatrix}
1 & 2 & 3 & | & 4 \\
0 & -4 & -8 & | & -12 \\
0 & -8 & -16 & | & -24 \\
\end{bmatrix}
$$
$$
\begin{align}
\xrightarrow {x_{2}\to \frac{x_{2}}{-4}} \\
\xrightarrow {x_{3}\to \frac{x_{3}}{-8}}
\end{align}
\begin{bmatrix}
1 & 2 & 3 & | & 4 \\
0 & 1 & 2 & | & 3 \\
0 & 1 & 2 & | & 3
\end{bmatrix}
\xrightarrow {\begin{align}
x_{1}\to x_{1}-2x_{2} \\
x_{3}\to x_{3}-x_{2}
\end{align}}
\begin{bmatrix}
1 & 0 & -1 & | & -2 \\
0 & 1 & 2 & | & 3 \\
0 & 0 &0 & | & 0
\end{bmatrix}
$$
We can now write this in typical notation:
$x_{1}-x_{3} = -2$
$x_{2} + 2x_{3} = 3$
We can rewrite this as 
$$
\begin{align}
x_{1}&=x_{3}-3 \\
x_{2}&=3-2x_{3}
\end{align}
$$
This has infinitely many solutions, which means that we have infinitely many ways of representing B with multiples of A. Thus, B is in the Span of A.



$$
\begin{align}

x_{1}-3x_{2}=-2 \\
x_{3}-2x_{4}=1\\

\left\{ \begin{bmatrix}
x_{1}\\x_{2}\\x_{3}\\x_{4}
\end{bmatrix} =  \begin{bmatrix}
-2 \\
0 \\
1 \\
0
\end{bmatrix} + \begin{bmatrix}
3 \\
1\\
0\\
0\\
\end{bmatrix} s_{1} + \begin{bmatrix}
0\\0\\1\\-2
\end{bmatrix}s_{2} : s_{1}\in \mathbb{R} \cap s_{2}\in \mathbb{R} \right\} 
\end{align}
$$