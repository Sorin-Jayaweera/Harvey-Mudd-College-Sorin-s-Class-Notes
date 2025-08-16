$$
\begin{align} \\
\text{ X marginal }
\begin{bmatrix}
x=0 & | & 0.16 \\
x=1 & | & 0.34 \\
x=2& | &  0.5\\
\end{bmatrix} \\
\text{ Y marginal } 
\begin{bmatrix}
y=0 & | & 0.24 \\
y=1 & | &  0.38\\
y=2 & | &  0.38\\
\end{bmatrix}
\end{align}
$$

$$
\begin{align}
P(y=1|x=0)=\frac{0.04}{0.16} =0.25\\
P(y=1|x=1)=\frac{0.2}{0.35} =0.571\\
P(y=1|x=3)=\frac{0.14}{0.5}=0.28
\end{align}
$$
We can see that all of these are different, meaning that Y is dependent on x. Therefore, these are dependent variables.


The expected value of each step in our walk is 
$$
\begin{align}
-\Delta x*P(-\Delta x)+\Delta x*P(\Delta x) \\
=-\Delta x * \frac{1}{2}+ \Delta x* \frac{1}{2} \\
= 0.
\end{align}
$$
The variance is given by 
$$
\begin{align}
\sigma & =\sqrt{ \frac{\left( -\frac{1}{2}-0 \right)^{2}+\left( \frac{1}{2}-0 \right)^{2}}{2} } \\
 & =\sqrt{ \frac{\frac{1}{4}+\frac{1}{4}}{2} } \\
 \sigma& =\frac{1}{4}
\end{align}
$$

The variance is given by 
$$

\begin{align}
\sigma^{2} & = \frac{\left( -\Delta x-0 \right)^{2}+\left( \Delta x-0 \right)^{2}}{2} \\
 & = \frac{2\Delta x^{2}}{2}  \\
 \sigma^{2}& =\Delta x^{2}
\end{align}
$$
The variance after n steps is 
$$
\begin{align}
n\sigma^{2} = n\Delta x^{2} \\
\text{ so we have the standard deviation } \\
\text{  after n steps being } \\
\sqrt{ n\sigma^{2} } = \sqrt{ n }x
\end{align}
$$



$$
\begin{align}
\text{ The markov tranition matrix P } \\
P=\begin{bmatrix}
 &| &1 & 2 & 3 \\
1 & | & 0.7 & 0.1 & 0.2\\
2 & | &  0.2 & 0.3 & 0.5\\
3 & | & 0.1 & 0.3 & 0.6\\   
\end{bmatrix}
\end{align}
$$

$P^{2}$ gives the transition from one state to the state after 2 days instead. 
Calculating this, we get
$$
\begin{align}
P^{2}=\begin{bmatrix}
0.53 & 0.16 & 0.31 \\
0.25 & 0.26 & 0.49 \\
0.19 & 0.28 & 0.53
\end{bmatrix}
\end{align}
$$
From here, we can read the probability of moving from sunny to rain in 2 days as $1\to 3=0.31$

$$
\begin{align}
P^{T=}\begin{bmatrix}
 &| &1 & 2 & 3 \\
1 & | & 0.7 & 0.2 & 0.1\\
2 & | &  0.1 & 0.3 & 0.3\\
3 & | & 0.2 & 0.5 & 0.6\\   
\end{bmatrix} \\
\text{ we choose the eignenvalues 1 } \\
\det(P^{T}-\lambda I)=0 \\
\begin{bmatrix}
0.7-1  & 0.2 & 0.1\\
 0.1& 0.3-1& 0.3 \\
 0.2& 0.5 & 0.6-1
\end{bmatrix}=0 \\
\end{align}
$$
We now row reduce this

$$
\begin{align}
\begin{bmatrix}
-0.3 & 0.2 & 0.1 & | & 0\\
0.1 & -0.7 & 0.3 & | & 0 \\
0.2 & 0.5 & -0.4 & | & 0
\end{bmatrix} \to   \\
\begin{bmatrix}
 1 & 0 & -\frac{13}{19} \\
0 & 1 & -\frac{10}{19} \\
0 & 0 & 0
\end{bmatrix}
\end{align}
$$

This gives us the eigenvectors $$
\begin{align}
\begin{bmatrix}
\frac{13}{19} \\
\frac{10}{19} \\
1
\end{bmatrix} \\
\text{ which normalizes to } \\
\frac{1}{3\sqrt{ 70}}\begin{bmatrix}
13\\10\\19
\end{bmatrix}
\end{align}
$$



