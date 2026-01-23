Ions in a Tokemac, electrons in a quantum computer, planets - they all look (on some level) like masses on springs. This is extremely useful.

Lets set up a system:
![[Pasted image 20251015150001.png|500]]

This has two degrees of freedom.

General steps:
1) choose some coordinates to write the $\mathscr{L}$
2) Get $E-L$ equations of motion
3) Solve for the equilibrium positions $(x_{1,0},x_{2,0})$
4) Expand the $\mathscr{L}$ (or Euler Lagrange equations) around the equilibrium, and switch to coordinates $\delta x_{1}=x_{1}-x_{1,0}$, etc.

The equilibrium positions from the system is different from the equilibrium of each string, but it doesn't matter! When we write out the force from each spring, we'll get something like
$$
\begin{align}
F=-k(x_{0}+x)
\end{align}
$$
Which has a constant term and a regular spring potential - but the net force in equilibrium is zero, so when we take all of these constant terms from each spring, they will net zero. This makes our overall force just the deltas away from system equilibrium for each spring - nice!

We have a potential term for each spring.
$$
\begin{align}
U=\underbrace{ \frac{1}{2}k(x_{1}) }_{ u_{1} } + \frac{1}{2}kx_{2}^{2}+\frac{1}{2}k'(x_{2}-x_{1})^{2} \\
T = \frac{1}{2}m\dot{x}_{1} ^{2}+\frac{1}{2}m\dot{x}_{2} ^{2} \\
\mathscr{L} = \frac{1}{2}m\dot{x}_{1} ^{2}+\frac{1}{2}m\dot{x}_{2} ^{2} -  \frac{1}{2}k(x_{1})+ \frac{1}{2}kx_{2}^{2}+\frac{1}{2}k'(x_{2}-x_{1})^{2}
\end{align}
$$
The thing that makes this problem hard is the coupling term between the two oscillators, which only appears on in the $\frac{1}{2}k'(x_{2}-x_{1})^{2}$ term, as it expands to $x_{1}^{2}-\underbrace{ 2x_{1}x_{2} }_{ \text{ makes this problem hard } }+x_{2}^{2}$.
We write out the E-L equations:
$$
\begin{align}
m \ddot{x_{1}}  & = -kx_{1}-k'x_{1}+k'x_{2}= -kx_{1}-k'(x_{1}-x_{2}) \\
m \ddot{x_{2}}  & = -kx_{2}-k'x_{2}+k'x_{1} = -kx_{2}+k'(x_{1}-x_{2})
\end{align}
$$
We can write this nicely with the new coordinates. Lets add together the two equations
$$
\begin{align}
x_{+} = x_{1}+x_{2} \\

m(\ddot{x_{1}}+\ddot{x_{2}})=-k(x_{1}+x_{2})
\end{align}
$$
This gives
$$
\begin{align}
x_{+} = A_{+} \cos(\omega_{+} t+\delta_{+} )
\end{align}
$$
where $\omega_{+}= \sqrt[]{ \frac{k}{m} }$

Lets also do the difference, $x_{1}-x_{2}$
$$
\begin{align}
m(\ddot{x}_{1} -\ddot{x}_{2} ) = -k(x_{1}-x_{2})-2k'(x_{1}-x_{2})
\end{align}
$$

Lets call this $x_{-}$
$$
\begin{align}
x_{-} (t) = A_{-} \cos(\omega_{-} +\delta_{-} ) 
\end{align}
$$
but now $\omega_{-}= \sqrt[]{ \frac{k+2k'}{m} }$

Now that we have $x_{+} \text{ and } x_{-}$, we can write uncoupled equations of motion. We call these $x_{+}\text{ and } x_{-}$ the normal modes (or eigen modes) of the system.

We can go back with $x_{1}=\frac{x_{+}+x_{-}}{2}$ and $x_{2}= \frac{x_{+}-x_{-}}{2}$.

We can write the solution as a matrix.
$$
\begin{align}
\mathbb{X}(t) = \begin{pmatrix}
x_{1}(t)\\ x_{2}(t) 
\end{pmatrix}  = \begin{pmatrix}
\frac{A_{+}}{2} \cos(\omega_{+} t+\delta_{+} ) + \frac{A_{-}}{2}\cos(\omega_{-} t+\delta_{-} ) \\
\frac{A_{+}}{2} \cos(\omega_{+} t+\delta_{+} ) - \frac{A_{-}}{2}\cos(\omega_{-} t+\delta_{-} ) \\
\end{pmatrix}
\end{align}
$$
Lets try to solve this. Lets choose the two masses starting at the same initial offset $x_{0}$, from rest.
$$
\begin{align}
x_{1} (0) = x_{2} (0) = x_{0}\\
\dot{x}_{1} (0) = \dot{x}_{2} (0) = 0
\end{align}
$$
Lets solve for $A_{+}$,$A_{-}$, $\delta_{-}$, $\delta_{+}$ first so that we can actually use this system.

We can take time derivatives to solve for the $\dot{x}$ part. The derivatives are sins. The sum and the difference of both sins has to be zero, so $\delta_{+}=\delta_{-}=0$, or we could say that $A_{-}=0$ and allow a value - keep that in mind. 

We can also plug in the initial position at $t=0$
$$
\begin{align}
x_{1}(0)=x_{0} = \frac{A_{+}}{2} \cos(\delta_{+} ) + \frac{A_{-}}{2}\cos(\delta_{-} ) \\
x_{2}(0)=x_{0} = \frac{A_{+}}{2} \cos(\delta_{+} ) - \frac{A_{-}}{2}\cos(\delta_{-} )
\end{align}
$$
From those two we get $A_{+}=2x_{0}$ and $A_{-}=0$

We have eigenmodes 
$$
\begin{align}
\begin{pmatrix}
1 \\ 1 
\end{pmatrix} \text{ and }   \begin{pmatrix}
1\\-1
\end{pmatrix}
\end{align}
$$
We write this by breaking out the $\mathbb{X}(t)$ as a vector sum of the $A_+$ and $A_{-}$ parts
$$
\begin{align}
\mathbb{X}(t) = \frac{A_{+}}{2} \begin{pmatrix}
1 \\ 1 
\end{pmatrix} \cos(\omega_{+} t + \delta_{t} ) + \frac{A_{-}}{2} \begin{pmatrix}
1 \\ -1 
\end{pmatrix} \cos(\omega_{-} t + \delta_{-} )
\end{align}
$$


### Useful math trick
We can write 
$$
\begin{align}
x_{-} = Re[z_{0}(t)] \\
A_{-} \cos(\omega_{-} t+\delta_{-} )= Re(A_{-} e^{i(\omega_{-}t+\delta_{-} )})  \\
\end{align}
$$
We can pull out the initial conditions and combine to get
$$
\begin{align} \\
c_{-} = A_{-} e^{i\delta_{-} } \\
= \pu{ Re }[C_{-} e^{i\omega_{-} t}]
\end{align}
$$
We can just write this as a complex number 
$$
\begin{align}
\underbrace{ A_{-} \cos\delta_{-}  }_{  a }+i\underbrace{ A_{-} \sin\delta_{-}  }_{ b } \\
a+bi
\end{align}
$$
