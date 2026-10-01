
on $\mathbb{C}^{2}$

Lets take a number $z=x+iy$, with angle (argument) $\alpha$ and length $\left| z \right|= (z^{*}z)^{\frac{1}{2}}$, and $z^{*} = x-iy$. 

We can have functions of complex variables, so we think of functions $\Omega(z,z^{*})$. Something magical happens when we think of functions which only depend on z -$\Omega(z)$.
$$
\begin{align}
\frac{ d \Omega}{d z^{*} } = & 0
\end{align}
$$


if we have 
$$
\begin{align}
\Omega = u + i \nu \\
\frac{ \partial \Omega }{ \partial z^{*} } = 0  \\
\implies \left( \frac{ \partial  }{ \partial x } + i \frac{ \partial  }{ \partial y }  \right)(u + i\nu) = 0
\end{align}
$$
This is the chain rule. We therefore have
$$
\begin{align}
\frac{ \partial  }{ \partial z^{*} } = \frac{ \partial x }{ \partial z^{*} } \frac{ \partial  }{ \partial x } + \frac{ \partial y }{ \partial z^{*} } \frac{ \partial  }{ \partial y } 
\end{align}
$$

The inverse relationships of $x$ and $y$ for $z$ and $z^{*}$ are
$$
\begin{align}
x = \frac{z+z^{*}}{2}, y = \frac{z-z^{*}}{2i}
\end{align}
$$
Using this, we have
$$
\begin{align}
\frac{ \partial  }{ \partial z^{*} } = \frac{1}{2}\frac{ \partial  }{ \partial x } + \frac{i}{2} \frac{ \partial  }{ \partial y } 
\end{align}
$$
We have two things that should sum to zero seperately:
$$
\begin{align}
\frac{ \partial u }{ \partial x } + i \frac{ \partial \nu }{ \partial x } + i \frac{ \partial u }{ \partial y } - \frac{ \partial \nu }{ \partial y } =0 \\
\frac{ \partial u }{ \partial x } = \frac{ \partial \nu }{ \partial y } \text{ and } \frac{ \partial \nu }{ \partial x } = - \frac{ \partial u }{ \partial y }   
\end{align}
$$

Lets take a derivative of each of these terms
$$
\begin{align}
\frac{ \partial^{2}u }{ \partial x^{2} } = \frac{ \partial^{2}\nu }{ \partial x\partial y } \\
\frac{ \partial^{2}\nu }{ \partial y\partial x } = - \frac{ \partial^{2}u }{ \partial y^{2} }   
\end{align}
$$
That means that
$$
\begin{align}
\frac{\partial^{2}\nu}{\partial x^{2}}+ \frac{\partial^{2}u}{\partial y^{2}} = 0
\end{align}
$$
This is laplaces equation! The laplaces equation that we have been solving before is just the real part of this holomorphic function! 


On the complex plane, differential equations become algebraic equations and 