---
lecture: phys-51-6
---

Recall, $$
\begin{align}
\nabla   & \text{ is a vector operator.  It acts as } \\
\vec{\nabla}\cdot \vec{c} & =\ text{ divergence (vector}\rightarrow  \text{ scaler) } \\
\vec{\nabla} \times  \vec{c} & =\text{ curl (vector }\rightarrow  \text{ vector) } \\
\vec{\nabla}f & =\text{ divergence (scalar}\rightarrow  \text{ scalar) }
\end{align}
$$
Also take the math facts that

$$
\begin{align}
\vec{\nabla}=\left\{ \hat{x} \frac{ \partial  }{ \partial x }  +\hat{y}\frac{ \partial  }{ \partial y } +\hat{z}\frac{ \partial  }{ \partial z } \right\} \\
\vec{ds} =dx \hat{x} + dy \hat{y} + dz \hat{z}
\end{align}
$$


##### _Definition_ Electrostatic potential:
$$
\begin{align}
V=\frac{u_{e}}{q_{0}}, \text{ like } \vec{E}= \vec{\frac{F_{e}}{q_{0}}} \\
v(b)-v(a)=\int_{a}^{b} \vec{E}\cdot \vec{ds}, \vec{E}=-\vec{\nabla}v 
\end{align}
$$

Lets review gravitational potential energy. 
$$
\begin{align}
\int_{a}^{b}-\vec{F}\cdot \vec{ds} = \int_{a}^{b} -mg(\hat{z})\cdot(dx \hat{x}+dy \hat{y}+dz \hat{z}) \\
\int_{a}^{b} mgdz=mgz \bigg|_{a}^{b} =mgb-mga \\
= U_{g}(a)-U_{g}(b) \\
\end{align}
$$
$$
\begin{align}
\vec{F}_{g} \text{  is a conservative force, so it is path independent } \\
\text{ no work for a closed path } \\
\vec{F}_{g}=-\vec{\nabla}U_{g}
\end{align}
$$

Now onto electrostatic potential. Lets imagine a point charge in a field. Lets take a test charge  along some path, with $\vec{ds}$ being a little step along that path.
$$
\begin{align}
\vec{F}_{e}=\frac{q_{0}q}{4\pi\epsilon_{0}r^{2}}\hat{r}
\end{align}
$$
The work done by an external agent would have to apply the opposite of this force to work against it.
This gives us the path integral
$$
\begin{align}
\int_{a}^{b} -\vec{F}_{e}\cdot \vec{ds}  \\
\text{ we can rewrite this in spherical coordinates } \\
\int_{}^{} -\frac{q_{0}q}{4\pi\epsilon_{0}r^{2}}\hat{r}\cdot(d\vec{r}\hat{+rd\theta \hat{\theta}} + r\sin\theta d\phi \hat{\phi})
\end{align}
$$
Note that this is physicist theta and physicist phi.
![[Pasted image 20240912095925.png]]

We can now calculate this.
$$
\begin{align}
\int_{a}^{b} -\vec{F_{e}} & \cdot \vec{ds}  \\
= -\frac{q_{0}q}{4\pi\epsilon_{0}}\left[ -\frac{1}{r} \right]_{a}^{b}  \\
= \frac{q_{0}q}{4\pi\epsilon_{0}}\left( \frac{1}{b}-\frac{1}{a} \right)  \\
= U_{e}(b)-U_{e}(a)
\end{align}
$$
This beautifully mimics what we see with gravity, so $\vec{F}_{e}$ is a conservative force and is path independent.

What happens if we have more then one point charge?
![[Pasted image 20240912100842.png]]
Imagine that we have nothing in the universe, and from infinity we stick $q_{1}$. This is "free", it doesn't have any work required.

Then we bring $q_{2}$ in, requiring work. This work is $$
\begin{align}
\int_{\infty}^{r_{1,2}} -\frac{q_{1}q_{2}}{4\pi\epsilon_{0}r^{2}}\hat{r}\cdot (dr \hat{r} + r d\theta \hat{\theta} + r\sin\theta d\phi \hat{\phi})  \\
=\frac{q_{1}q_{2}}{4\pi\epsilon_{0}}\left( \frac{1}{r_{1,2}}-\frac{1}{\infty} \right)
\end{align}
$$

$$
\begin{align}
q_{3} \text{ requires: }  \\
-\int (\vec{F}_{e_{1,3}}+\vec{F}_{e_{2,3}})  \\
\text{ note that they have different  }\hat{r}\text{ since the field  } \\
\text{ originates from different points }  \\
\frac{1}{4\pi\epsilon_{0}}\left( \int_{path}^{}q_{1}q_{3}\hat{r}\cdot \vec{ds} +\int_{path}^{}q_{2}q_{3}\hat{r}\cdot \vec{ds}   \right)   \\
= \frac{1}{4\pi\epsilon_{0}}\left( -q_{1}q_{3} \int_{\infty}^{r_{1,3}} \frac{dr}{r^{2}}-q_{2}q_{3}\int_{\infty}^{r_{2,3}} \frac{dr}{r^{2}} \right)  \\
= \frac{1}{4\pi\epsilon_{0}}\left( \frac{q_{1}q_{3}}{r_{1,3}}+\frac{q_{2}q_{3}}{r_{2,3}} \right)
\end{align}
$$
The total potential energy is
$$
\begin{align}
\frac{1}{4\pi\epsilon}\left( \frac{q_{1}q_{2}}{r_{1,2}}+\frac{q_{1}q_{3}}{r_{1,3}}+\frac{q_{2}q_{3}}{r_{2,3}} \right) 
\end{align}.
$$
In general, we just have all the combinations of charge from each point interacting with each other as the total electrostatic potential.

We can now use what we've learned to motivate another one of Maxwell's equations.
While we are in electrostatics, meaning that nothing is changing with time, we can write that 

This one is called Faraday's Law.
$$
\begin{align}
\oint\vec{E}\cdot \vec{ds} =0. \\
\vec{E}=-\vec{\nabla}V
\end{align}
$$
In the near future, we'll have the differential form that 
$$
\begin{align}
\nabla \times  E=0
\end{align}
$$
The implication of these is that if there is a conductor with a hole, there can't be any net charges or fields on the inside of the conductor, because we can't draw a closed path while having it integrate to zero. As long as the charge on the inside is net 0, the conductor is not effected.


The potential of a continuous charge distribution is
$$
\begin{align}
dv=\frac{dq}{4\pi\epsilon_{0}r}
\end{align}
$$

Lets do an example of a ring of uniform charge.
![[Pasted image 20240912105041.png]]![[Pasted image 20240912105051.png]]
![[Pasted image 20240912105118.png]]

See previous: [[Differential Form of Gauss's Law]]
See next: [[More on the electrostatic field]]
