1) Objects of different masses all fall with $a = g$
2) Keplers laws of planeary motion
	1) Planets travel in ellipses
	2) Planets sweep out equal areas in equal times
	3) $P_{orb}^{2} \propto a^{3}$


Lets look at the Two Body Problem.

With two bodies, there are 6 degrees of freedom - $(x_{1},y_{1},z_{1},x_{2},y_{2},z_{2})$.

We have six coupled differential equations to solve at the same time, that look like
$$
\begin{align}
\ddot{x_{1}} = \dots \\
\ddot{y_{1}} = \dots \\
\ddot{z_{1}} = \dots \\
\ddot{x_{2}} = \dots \\
\ddot{y_{2}} = \dots \\
\ddot{z_{2}} = \dots \\
\end{align}
$$

This would be really difficult, but it has such a simple solution (ellipses!) even though its nearly always impossible to solve such massive diff eqs analytically. 

We have cyclic variables (which correspond to conserved quantities)
$$
\begin{align}
\vec{r_{1}},\vec{r_{2}} \to &    \\
 & \vec{r} = \vec{r_{2}}- \vec{r_{1}}  \\
 & \vec{R}_{cm} 
\end{align}
$$
$R_{cm}$ is cyclic, so $P_{com,x,y,z}$ (linear momentum of the center of mass) is conserved. This means that those three coordinates will just be moving in a straight line depending on the initial conditions. We now have to solve for the other three degrees of freedom. 

This means that we can break up our Lagrangian into parts that are more intuitive:
$$
\begin{align}
\mathscr{L} = \mathscr{L}_{com} + \mathscr{L}_{rel}  
\end{align}
$$
where $\mathscr{L}_{com}$ is as if its the motion of one body, and $\mathscr{L}_{rel}$ is the displacements relative to that center of either body.

We now have an equivalent one body problem for the $\mathscr{L}_{com}$.

We write 
$U(r)=-\frac{Gm_{1}m_{2}}{r}=-G \frac{M\mu}{r}$
$$
\begin{align}
\frac{GM}{r} \frac{m_{1}m_{2}}{m_{1}+m_{2}} = \frac{Gm_{1}m_{2}}{r}  \\
\implies M = m_{1}+m_{2}
\end{align}
$$

So we can write out the piece of the Lagrangian that care about this
$$
\begin{align}
\mathscr{L}_{com} = \frac{1}{2}(M)\left| \vec{\dot{R}}_{cm}  \right| ^{2}   
\end{align}
$$


Now lets take care of the relative component.

We now have to solve for the motion of the "fake" mass $\mu$. $\mu$ is defined by velocity and acceleration. These are two vectors with three elements each - and linear combinations of the two vectors can only span a plane. This is special, because we can reduce from 3 dimensions down to 2 by a careful choice. 
Lets take some rotated coordinate axes $x',y',z'$, but where in the new frame $z'=0$ always. In this new coordinate axis, we can really just specify things as $r$ and $\theta$, since its a plane. For that plane, we have
$$
\begin{align}
\mathscr{L} = \frac{1}{2} \mu(\dot{r}^{2}+ r^{2}\dot{\phi}^{2}) - u(r)
\end{align}
$$
We see that $\phi$ doesn't appear but $\dot{\phi}$ does, so it must be cyclic.
We don't have time dependence in the coordinate system (from cartesian to polar here), so the Hamiltonian is just
$$
\begin{align}
\mathcal{H}  & = T+U  \\
 & = \frac{1}{2}\mu \dot{r}^{2} + \frac{1}{2} \mu r^{2} \dot{\phi}^{2} + u(r)
\end{align}
$$
and the constant angular momentum is
$$
\begin{align}
\mathscr{l} = \frac{ \partial \mathscr{L} }{ \partial \dot{\phi} } = \mu r^{2} \dot{\phi}
\end{align}
$$

We can solve for $\dot{\phi}$ in the $\mathscr{l}$ equation. 
$$
\begin{align}
\dot{\phi} = \frac{\mathscr{l}}{\mu r^{2}}
\end{align}
$$
Using that in the Hamiltonian
$$
\begin{align}
\mathcal{H}= \frac{1}{2}\mu \dot{r}^{2} + \frac{1}{2}mr^{2} \mathscr{l} \frac{^{2}}{\mu^{2}r^{4}} + u(r) \\
\mathcal{H} = \frac{1}{2} \mu \dot{r}^{2} + \frac{1}{2}  \frac{\mathscr{l}^{2}}{\mu r^{2}}+ u(r)
\end{align}
$$

We can make up one more fictitious problem to make this easier to solve.
We notice that only two terms depend on $r$, and we have a kinetic energy. This looks like
$\mathcal{H}= T + U_{eff}(r)$
That's a ball of mass $\mu$ rolling around in a potential field $U_{eff}$.

Lets write this explicitely:
$$
\begin{align}
U_{eff}(r) =\frac{\mathscr{l}^{2}}{2\mu r^{2}} - \frac{\overbrace{GM\mu}^{+\alpha}}{r}
\end{align}
$$
We can think about both of these terms and how they explode at zero vs where they converge at $r\to \infty$.
![[Pasted image 20250922154839.png|400]]

So this would look like the earth moving towards and away from the sun in a potential well (or the reduced mass moving towards the center and away). If we start off with $H>0$ then we aren't in a bound state and the masses would shoot away. If $H<0$ then we are bound to nice solutions.

If we can figure out $r(t)$, we know what phi is to conserve angular momentum. For really large r, that's a slow $\dot{\phi}$, for small $r$ that's a huge $\dot{\phi}$.


We can note the minimum of this energy. If the distance from the sun never changes, then it just traces out a circle. 

This is at 
$u_{0}= -\frac{\mu \alpha^{2}}{2 \mathscr{l}^{2}}$ and $r_{0} = \frac{\mathscr{l}^{2}}{\mu \alpha}$

$$
\phi = \int dt \frac{\mathscr{l}}{\mu r^{2}} 
$$







$$
\begin{align}
\mathscr{L}=\underbrace{ \frac{1}{2}(M)\left| \vec{\dot{R}}_{cm}  \right| ^{2} }_{ \mathscr{L}_{com}  } + \frac{1}{2}\mu \left| \dot{r} \right| ^{2} - u(\left| \vec{r} \right| ) \\
\text{ where} \\
\mu = \frac{m_{1}m_{2}}{m_{1}+m_{2}}
\end{align}
$$
