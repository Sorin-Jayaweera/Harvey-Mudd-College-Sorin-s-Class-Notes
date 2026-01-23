We can reduce the orbits of planets or plasma resonances -- basically everything chaotic -- as some pendulum dynamics.

## SHO 
If we have a spring with constant $k$ and mass $m$, 
$$
\begin{align}
\omega_{0}^{2}= \frac{k}{m}
\end{align}
$$
$$
\begin{align}
\ddot{x}= -\frac{k}{m}, x = -\omega^{2}x
\end{align}
$$
$$
\begin{align}
x(t) = A\cos(\omega_{0}t+\gamma)
\end{align}
$$

With period $\frac{2\pi}{\omega}$.

![[Pasted image 20251006145210.png|300]]
We can draw level curves in state space where each level corresponds to energy.

The SHO is a linear oscillator, in that the time to traverse any curve is the same, independent of the energy. 
$$
\begin{align}
\ddot{x}= A\underbrace{ x' }_{ \text{ any linear function of x  } }
\end{align}
$$
where $x'$ is just a function of $x$ to the $1$. 

## Pendulum
![[Pasted image 20251006145535.png|300]]
$$
\begin{align}
\mathscr{L} = \frac{1}{2}ml^{2}\dot{\theta}^{2} - (-mgl\cos(\theta))
\end{align}
$$
We get
$$
\begin{align}
\frac{d}{dt} \left( \frac{ \partial \mathscr{L} }{ \partial \dot{\theta} }  \right) = \frac{ \partial \mathscr{L} }{ \partial \theta } \\
ml^{2} \ddot{\theta} = -mgl \sin\theta \\
\ddot{\theta} = -\frac{g}{l}\sin(\theta) = -\omega_{0}^{2}\sin(\theta) 
\end{align}
$$
The $\sin\theta$ expands to $\theta - \frac{\theta^{3}}{3} + \dots$ which is nonlinear but close enough for small angle. 

Normally the curves can't cross, since they tell you how the system will evolve and there can't be two unique paths from one spot. However, at equilibria points the system is stationary so it wouldn't move... so we can have crossings. 
![[Pasted image 20251006151717.png]]

Lets take
$$
\begin{align}
\frac{ d \theta}{d t } = -\omega_{0}^{2}\sin(\theta)
\end{align}
$$
Lets solve this the same was as we did the two body problem. Lets look for conserved quantities, i.e. Energy.
$$
\begin{align}
H= \frac{1}{2}ml^{2}\dot{\theta}^{2}-mgl\cos\theta
\end{align}
$$
We know that $H$ is constant, so
$$
\begin{align}
\frac{ d H}{d t } =0  \\
\frac{1}{2}ml^{2}\dot{\theta}^{2}=\underbrace{ H }_{ \text{ constant } }+mgl\cos\theta
\end{align}
$$

$$
\begin{align}
\frac{d}{dt} \theta = \left[ \frac{2H}{ml^{2}} + 2 \frac{g\cancelto{  }{ ml }\cos\theta}{\cancelto{  }{ m }l\cancelto{  }{ ^{2} }} \right]^{\frac{1}{2}}
\end{align}
$$
We have the integral now
$$
\begin{align}
\int_{\theta(t=0)}^{\theta(t)}  \frac{d\theta}{\left[ \frac{2H}{ml^{2}}+ \frac{2g}{l}\cos\theta \right]^{\frac{1}{2}}} = \int_{0}^{t} dt'
\end{align}
$$

Note that most of these are constants, its just an integral with $\theta$. 
We use a trig sub and get an elliptic function, where 
$$
\begin{align}
\theta(t) = (\text{ Elliptic function })^{-1}(t)
\end{align}
$$
This is gross and nasty -- looking at the state space to find if solutions are bounded or not is really nice. 

## Fixed Points
$$
\begin{align}
\ddot{\theta}= -\frac{g}{l}\sin\theta = -\omega_{0}^{2}\sin\theta \\
\omega_{0}^{2}= \frac{g}{l}
\end{align}
$$
The fixed points here happen at $\theta=n\pi, n \in\mathbb{N}$

For $\theta \text{ near  }0$ we have have the easy solution
$$
\begin{align}
\ddot{\theta}= -\omega_{0} \left( \theta \cancelto{  }{ - \frac{\theta^{3}}{3 }}\dots \right)
\end{align}
$$
This is stable, since the acceleration is in the opposite direction.

What if we are looking around $\theta=\pi?$
$$
\begin{align}
\ddot{\theta} = -\omega^{2}(\cancelto{  }{ \sin\theta_{0} } + \cos(\theta_{0})(\theta-\theta_{0})+\dots) \\
\ddot{\theta} = \omega^{2}(\theta-\theta_{0})
\end{align}
$$
This is an unstable equilibrium, since we are pushed away as changes increases. 
$$
\begin{align}
\delta\theta = \theta-\theta_{0} \\
d \ddot{\theta} = \ddot{\theta}\cancelto{ 0 }{ - \ddot{\theta_{0}} } = \omega_{0}^{2}\delta\theta
\end{align}
$$
This changes our origin from being at zero to being at pi. 

We write 
$$
\begin{align}
\delta\theta(t) = Ae^{\omega_{0}t} + Be^{-\omega_{0}t}
\end{align}
$$

The A term explodes as time goes larger, so we wouldn't stay there. That is the "unstable manifold". On the unstable manifold, as time increases we get further from the fixed point. The B term disappears as time increases.

Another perspective is that $A$ takes you away from the equilibrium going forwards in time, but the $B$ term takes you away going backwards in time. 

At the stable points, we have a crossing 
![[Pasted image 20251006155207.png|500]]



