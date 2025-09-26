Laplaces equation
$$
\begin{align}
\nabla^{2}V = 0 \\
\frac{ d^{2} V}{d x^{2} } + \frac{ d^{2} V}{d y^{2} } + \frac{ d ^{2}V}{d z^{2} }  =0
\end{align}
$$
This can only have a maximum at extrema, as the derivatives have to be zero.

Take a 2d box with 3 grounds and an electrode on the top.

$$
\begin{align}
V_{xx} + V_{yy}=0 \\
V(x,y) =X(x)Y(y) \\
\frac{X''Y+Y''X}{XY} = 0   \\
\frac{X''}{X}+\frac{Y''}{Y}=0
\end{align}
$$

One is positive, the other is negative. The positive will be an oscillatory function, and the other will be a decaying exponential.
![[Pasted image 20250410094553.png]]
Lets make the oscillatory condition in the X, since a sin wave can be zero at both grounded parts. 

We have

$$
\begin{align}
X(x)= \sin\left( \frac{n\pi x}{L} \right)
\end{align}
$$
Plugging in this solution, we can find $Y:$
$$
\begin{align}
\frac{-n^{2}\pi^{2}}{L^{2}}+ \frac{n^{2}\pi^{2}}{L^{2}}=0
\end{align}
$$
So 
$$
\begin{align}
Y'' = \frac{n^{2}\pi^{2}}{L^{2}}Y \\
Y = e^{\pm  n\pi \frac{y}{L}}
\end{align}
$$
this gives 
$$
\begin{align}
Y(y)= \sinh\left( \frac{n\pi y}{L} \right)
\end{align}
$$
since 
$$
\begin{align}
\sinh(z)= \frac{e^{z}-e^{-z}}{2}
\end{align}
$$
We have to satisfy $y=0$ gets zero, and sinch is a nice standard. 

We can write out now,
$$
\begin{align}
V(x,y)= \sum_{n=1}^{\infty} a_{n}\sin\left( \frac{n\pi x}{L} \right) \sinh\left( \frac{n\pi y}{L} \right) 
\end{align}
$$
Each term is a harmonic function. The Laplacian of each term will get zero.


For arbitrary x but $Y=L$, the function has to equal $V_{0}$.

We have
$$
\begin{align}
V(x,L)=V_{0}= \sum_{n=1}^{\infty} a_{n}\sin\left( \frac{n\pi x}{L} \right)\sinh(n\pi)
\end{align}
$$
Lets multiply both sides by $\sin\left( \frac{m\pi x}{L} \right)$ and integrate, since sin(m) and sin(n) are orthogonal except when they equal.

$$
\begin{align}
\int_{0}^{L} V_{0}\sin\left( \frac{m\pi x}{L} \right)dx & = \sum_{n=1}^{\infty} \int_{0}^{L} a_{n}\sin\left( \frac{n\pi x}{L} \right)^{2} \sinh(n\pi)dx \\
 & = \delta_{nm} \frac{L}{2}a_{n} \sinh(n\pi)
\end{align}
$$
The left side is
$$
\begin{align}
v_{0} - \frac{\cos\left( \frac{m\pi x}{L} \right)}{\frac{m\pi}{L}}\bigg|_{0}^{L}  = \frac{v_{0}L}{m\pi}(1-(-1)^{m})
\end{align}
$$
This is nonzero when $m$ is odd. 
In that case, we get
$$
\begin{align}
 \frac{2v_{0}L}{m\pi}= \frac{a_{m}L}{2} \sinh(m\pi) \\
a_{m} = \begin{cases}
\frac{4v_{0}}{m\pi \sinh (m\pi)} & \text{ when m is odd }  \\
0  & \text{ even }
\end{cases}
\end{align}
$$
This gives us
$$
\begin{align}
V(x,y) = \frac{4V_{0}}{\pi} \sum_{n \text{ odd }}^{\infty} \frac{\sin\left( \frac{n\pi x}{L} \right)\sinh\left( \frac{n\pi y}{L} \right)}{n\sinh(n\pi)}
\end{align}
$$


