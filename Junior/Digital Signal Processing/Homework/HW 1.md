
![[Pasted image 20260120110106.png]]

The basis vectors $v_{k}$ of the DFT are $e^{-j \frac{2\pi}{N}nk}$

We can check the first relation. Instead of $i$ and $j$ I will use the variables $n \text{ and }  m$.

We define the inner product as the sum from $k=0$ to $k=N$.

$$
\begin{align} 
v_{n}^{\dagger}v_{m} & = \\  
 & =\sum_{k=0}^{N-1} \left( e^{-j \frac{2\pi}{N}kn}  \right)^{\dagger} e^{-j \frac{2\pi}{N}km} \\
 & =\sum_{k=0}^{N-1} e^{j \frac{2\pi}{N}k (m-n)} \\
\end{align}
$$

This is a geometric series 
$r=e^{\left( j\frac{2\pi}{N}(n-m) \right)}$ and $a=1$.
This converges to
$$
\begin{align} 
 & \, \, \, \, \, \, \frac{1- r^{N}}{1-r}\\
 & =\left( \frac{1- e^{j \frac{2\pi}{N}(n-m)^{N}}}{1-e^{j \frac{2\pi}{N}(n-m)}} \right) \\
& =\left( \frac{1- e^{j 2\pi(n-m)}}{1-e^{j \frac{2\pi}{N}(n-m)}} \right)
\end{align}
$$


For the case $m\neq n$, The numerator is $(1-e^{j 2\pi (n-m)})$. N and M are integers, so this is equivalent to $1-e^{j 2\pi}=0$.


if $n=m$, then $r=e^{j 2\pi(0)}=1$. The Geometric series for $r=1$ is $\sum_{k=0}^{N-1}1=N$.

Because the inner product is the $\text{ Euclidian length }^{2}$,  the length of the basis vector $v_{i}=\sqrt[]{ N }$. 


*This is the first way I did it, which was convoluted but I think technically right. I realized when rereading wikipedia that the formula was different for $r=1$, which should have been obvious. I'm still proud of this below thing though, so I left it in*.
We can also see this as the result from analytic continuation (if we pretend that $M$ and $N$ are real instead of just integers). For the case $m\to n$, the series approaches  $\frac{0}{0}$. We can therefore use L'hopitals rule. This yields $N$, since the derivatives of the top and the bottom are the same (so dividing gets 1) except for the overall factor of N on the numerator. 





![[Pasted image 20260120110117.png]]
Intuitively:

For a real, double sided DFT indexed from highest negative frequency to zero to highest positive frequency, there is a reflection symmetry where X(highest positive frequency) = X(highest negative frequency), where the $\left| \text{ highest freq } \right|= \left| \text{ highest negative freq } \right|$.In index notation, with 0 at the highest negative frequency, this is
$X(k)=X(N-k)$

Assuming that $x[n]$ is real, we can check the equality by direct substitution
$$
\begin{align}
X[k] \stackrel{?}{=}  X^{*}[N-k] \\
\end{align}
$$

$$
\begin{align}
\sum_{n=0}^{N-1} x[n]e^{-j \frac{2\pi}{N}k_{n}}  & \stackrel{?}{=}  \left(  \sum_{n=0}^{N-1} x[n]e^{-j \frac{2\pi}{N}(N-k_{n})} \right)^{*}  \\
\text{ if x is real, then } x[n]^{*} & =x[n] \\
e^{-j \frac{2\pi}{N}k_{n}}  & \stackrel{?}{=}    e^{-j \frac{2\pi}{N}(k_{n}-N)} \\ 
 & \uparrow e^{-j \frac{2\pi}{N}N}e^{\frac{2\pi}{N}k_{n}}\\
1  & =   e^{-j 2\pi} \\
1 & =1
\end{align}
$$

Therefore, if $x[n]$ is real, then $X[k]=X^{*}[N-k]$.


![[Pasted image 20260120110125.png]]
We have the generic DFT matrix
$$
\begin{align}
\begin{bmatrix}
e^{-j \frac{2\pi}{N}} & e^{-j \frac{2\pi}{N}} &  \dots  & e^{-j \frac{2\pi}{N}(N-1)} \\
e^{-j \frac{2\pi}{N}\cdot0} & e^{-j \frac{2\pi}{N}\cdot 1}  & \dots  & e^{-j \frac{2\pi}{N}(N-1)}  \\
\vdots \\
e^{-j \frac{2\pi}{N}} & e^{-j \frac{2\pi}{N}1 \cdot(N-1)} & \dots &  e^{-j \frac{2\pi}{N}(N-1)^{2} }
\end{bmatrix} 
\end{align}
$$
The generic iDFT Matrix is:
$$
\begin{align}
\frac{1}{N} \begin{bmatrix}
e^{j \frac{2\pi}{N} \cdot 0}  & e^{j \frac{2\pi}{N} \cdot 0} &  e^{j \frac{2\pi}{N} \cdot 0} &  \dots &  e^{j \frac{2\pi}{N}\cdot 0} \\
e^{j \frac{2\pi}{N}\cdot 0} & e^{j \frac{2\pi}{N} \cdot 1}  &  e^{j \frac{2\pi}{N} \cdot 2}  & \dots  &  e^{j \frac{2\pi}{N} \cdot (N-1)} \\
e^{j \frac{2\pi}{N}\cdot 0} & e^{j \frac{2\pi}{N} \cdot 2}  &  e^{j \frac{2\pi}{N} \cdot 3}  & \dots &   e^{j \frac{2\pi}{N} \cdot 2(N-1)} \\ \\
\vdots \\
e^{j \frac{2\pi}{N}\cdot 0} & e^{j \frac{2\pi}{N} \cdot (N-1)}  &  e^{j \frac{2\pi}{N} \cdot 2(N-1)}  & \dots &   e^{j \frac{2\pi}{N}  \cdot  (N-1)^{2}}
\end{bmatrix}
\end{align}
$$

For both of these, down is wavenumber $k$ and across is sample number $n$.
Let $\mathcal{A}$ denote the DFT matric and $\mathcal{B}$ denote the iDFT matrix.


For $N=2$, this is:
$$
\begin{align}
\mathcal{A} =  \begin{bmatrix}
1 & 1 \\
1 & e^{-j\pi}
\end{bmatrix}
\end{align}
$$
$$
\begin{align}
\mathcal{B} = \frac{1}{2}\begin{bmatrix}
1 & 1  \\
1 & e^{j \pi}
\end{bmatrix}
\end{align}
$$
$$
\mathcal{AB} = \frac{1}{2}\begin{bmatrix}
1 & 1 \\
1 & e^{-j\pi} 
\end{bmatrix}\begin{bmatrix}
1 & 1 \\ 1 & e^{j\pi}
\end{bmatrix} = \begin{bmatrix}
1 & \frac{1+e^{j\pi}}{2} \\
\frac{1+e^{-j\pi}}{2} & 1
\end{bmatrix} = \begin{bmatrix}
1 & 0 \\ 0  & 1 
\end{bmatrix}
$$



For $N=3$, this is
$$
\begin{align}
\mathcal{A} = \begin{bmatrix}
1 & 1 & 1 \\
1 & e^{-j \frac{2\pi}{3}} & e^{-j \frac{4\pi}{3}} \\
1 & e^{-j \frac{4\pi}{3}} & e^{-j \frac{8\pi}{3}}
\end{bmatrix} \\
\mathcal{B}  = \frac{1}{3} \begin{bmatrix}
1 & 1 & 1 \\
1 & e^{j\frac{ 2\pi}{3}} & e^{j \frac{4\pi}{3}} \\
1 & e^{j \frac{4\pi}{3}} & e^{j \frac{8\pi}{3}}
\end{bmatrix}
\end{align}
$$

$$
\begin{align}
\mathcal{AB}  & = \frac{1}{3} \begin{bmatrix}
3 & 1 + e^{j \frac{2\pi}{3}} + e^{j \frac{4\pi}{3}}  &  1 + e^{j \frac{4\pi}{3}}+ e^{j \frac{8\pi}{3}} \\
1+e^{-j \frac{2\pi}{3}} + e^{-j \frac{4\pi}{3}} & 1 + e^{\frac{-2\pi}{3}}e^{j \frac{2\pi}{3}} + e^{-j \frac{8\pi}{3}}e^{j \frac{8\pi}{3}}  & 1+e^{-j\frac{ 2\pi}{3}}e^{j \frac{4\pi}{3}}+e^{-j \frac{4\pi}{3}} e^{j \frac{8\pi}{3}} \\
1+e^{-j \frac{4\pi}{3}}+e^{-j\frac{8\pi}{3}} & 1+e^{-j\frac{4\pi}{3}}e^{\frac{2\pi}{3}}+ e^{-j\frac{8\pi}{3}}e^{j \frac{4\pi}{3}} & 1+e^{\frac{-4\pi}{3}}e^{\frac{4\pi}{3}}+e^{\frac{-8\pi}{3}}e^{\frac{8\pi}{3}}
\end{bmatrix} \\
 & = \begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix}
\end{align}
$$



![[Pasted image 20260120110132.png]]

![[Pasted image 20260123154525.png]]


![[Pasted image 20260120110142.png]]

The Fourier series is computed in order from 0 to high frequency, and then continuing higher - at frequencies that wrap around and become negative. The two sided plot would cut this at the center and move it left. We have the highest positive and negative frequencies at the center, where there is low signal power. This data is not very useful, and can be cut. 

![[Pasted image 20260120173255.png]]
![[Pasted image 20260120173232.png]]
![[Pasted image 20260120173213.png]]
![[Pasted image 20260120110154.png]]
