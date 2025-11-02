Lets model scattering a particle off of a hard glass ball, and generalize to any central force potential.



![[Pasted image 20250929150346.png|500]]


We know that we must conserve angular momentum and energy. The outgoing trajectory must have the same $v_{\infty}$ and $\beta$ offset from the line of symmetry. 

Lets say that our potential is 0 if there is no collision, of $\infty$ if we hit the big ball.
$$
\begin{align}
u(r) = \begin{cases}
0 & r>R \\
\infty & r \leq R
\end{cases}
\end{align}
$$

Our goal is to find the scattering angle in terms of the impact parameter $b$ (off axis distance) and $v_{\infty}$. 

First off, we know that $2\beta+\theta=\pi$, so $\beta= \frac{\pi}{2}-\frac{\theta}{2}$

Also, we know that
$$
\begin{align}
\sin(\beta) = \frac{b}{R}
\end{align}
$$
If $b>R$, we know that there will be no deflection (because no collision), so
$$
\begin{align}
\sin\left( \frac{\pi}{2} - \frac{\theta}{2} \right) = \frac{b}{R} \\
\cos\left( \frac{\theta}{2} \right) = \frac{b}{R} \\
\theta = \begin{cases}
2\cos ^{-1}\left( \frac{b}{R} \right) & \text{ if b<R } \\
0 & \text{ else }
\end{cases}
\end{align}
$$

## Rutherford Scattering
Lets take the "plum pudding model"
This was disproven by rutherford scattering, when $He^{2+}$ bounce off of the nuclei of atoms with heavy scattering angles instead of passing straight through the gold sheet.

We are now using the potential
$u(r) = \frac{-\alpha}{r}$.
This looks like gravity or coulomb potential
$$
\begin{align}
-\frac{G(m_{1}m_{2})}{r} \\
\frac{1}{4\pi\epsilon_{0}} \frac{q_{1}q_{2}}{r}
\end{align}
$$
so we set $\alpha= -\frac{1}{4\pi\epsilon_{0}} q_{1}q_{2}$
so that we can reuse our results from gravitational potential.

Because make $\alpha<0$ that this is a repulsive force.

Our closest approach, through which there is a line of symmetry, is where $\phi=0$. We define theta going to the right so that theta = 0 yields $-r_{min}$ which gets us to the right direction. 

![[Pasted image 20250929152007.png|400]]

We have, from geometry, 
$$
\begin{align}
\beta= \pi-\phi \\
\beta = \frac{\pi}{2} - \frac{\theta}{2}
\end{align}
$$


$$
\begin{align}
r = \frac{l^{2}/\mu \alpha}{1+e\cos(\phi)}
\end{align}
$$
The asymptotes are solutions for $r(\phi)=\infty$, so
$$
\begin{align}
1+e\cos(\phi) = 0 \\
\cos(\beta) = \frac{1}{e}
\end{align}
$$
where $e$ is the eccentricity. 

$$
\begin{align}
\cos\left( \frac{\pi}{2} - \frac{\theta}{2}  \right) = \frac{1}{e} \\
e = \frac{1}{\sin\left( \frac{\theta}{2} \right)} \\
e = \sqrt[]{ 1+\frac{2El^{2}}{\mu \alpha^{2}} }  \\
e^{2} = 1+ \frac{2El^{2}}{\mu \alpha^{2}} = \frac{1}{\sin ^{2}\left( \frac{\theta}{2} \right)} \\
\end{align}
$$
$$
\begin{align}
\frac{2El^{2}}{\mu \alpha^{2}} = \frac{1}{\sin ^{2}\left( \frac{\theta}{2} \right)} - \sin \frac{^{2}\left( \frac{\theta}{2} \right)}{\sin ^{2}\left( \frac{\theta}{2} \right)} \\
 = \cos \frac{^{2}\left( \frac{\theta}{2} \right)}{\sin ^{2}\left( \frac{\theta}{2} \right)} = \cot ^{2}\left( \frac{\theta}{2} \right) \\
\tan ^{2}\left( \frac{\theta}{2} \right) = \frac{\mu \alpha^{2}}{2El^{2}}
\end{align}
$$

$$
\begin{align}
\tan ^{2}\left( \frac{\theta}{2} \right) = \frac{\mu \alpha^{2}}{2 \left( \frac{1}{2} \mu v_{\infty} ^{2} \right)(\mu^{2}b^{2}v_{\infty} ^{2})} \\
\tan ^{2}\left( \frac{\theta}{2} \right) = \frac{\alpha}{\mu bv_{\infty} ^{2}}
\end{align}
$$
We have shown that
$$
\begin{align}
\theta = 2 \tan ^{-1}\left( \frac{\alpha}{\mu bv_{\infty} ^{2}} \right)
\end{align}
$$

Lets check units. $\alpha$ has $\pu{ energy*distance}$
$\mu v_{\infty}^{2}$ has units of energy, $b$ is distance, so the arguments of tan are properly unitless. 

The faster you go, the less you'll be effected (the ratio between your energy to the potential energy at the minimum gets better). The further from the center, also the less you'll care.  


## Two body problem summary
we have 6 degrees of freedom, but three quantities are conserved (momentum of the center of mass in x,y,z). We have three quantities which specify the $\vec{R}_{com}$. We change from $\vec{r}_{1},\vec{r}_{2}$ to $\vec{R}_{com} \text{ and } r$

Our Legrangian is
$$
\begin{align}
\mathscr{L} = \frac{1}{2}M_{tot} \left| \dot{\vec{R}_{com} } \right|^{2} + \frac{1}{2}\mu \left| \vec{r} \right| ^{2} - u(r) 
\end{align}
$$
In the center of mass frame, we have $\dot{\vec{R}}_{com}=0$
This leaves the nice $\mathscr{L}$
$$
\begin{align}
\mathscr{L} = \frac{1}{2} \mu \left| \vec{r} \right| ^{2} - u(r)
\end{align}
$$
We note that the two bodies must always lie in a plane because of the conservations, so we can rewrite the plane in terms of $i (\text{ inclination }),\phi'$. 

We have conservation of $\mathcal{H}$ (energy) and $\mathscr{l}= m\vec{r}\times \vec{v}$

Lets enumerate the conserved quantities:
$\vec{V}_{com}$ :3, x y z
$i,\phi'$ :2, defining the orbital plane
$\mathcal{H}$: Energy
$\mathscr{l}$: Angular momentum from the effective potential and kinetic

We've been dealing with a special system that is nice, but sometimes the pericenter (closest approach) shifts by some angle over time.
We define a new eccentricity where
$$
\begin{align}
\vec{e} = \left| e \right| \text{ in the direction of the pericenter }
\end{align}
$$ 
In our case, the $\vec{e}$ is constant - so this is another conserved quantity (the angle of the pericenter).

So we went from 12 independent variables down to 1 thing changing!


## Lets go to 3 bodies!

Lets consider Jupiter.
$\frac{M_{j}}{M_{\odot}}\approx 10^{-3}$
and Jupiter is ~ 4 au from earth, so
$\frac{F_{j}}{F_{sun}}\approx 10^{-3}$

Our conserved quantities will slowly change because of Jupiter.

We consider a smearing of mass in their orbits, so that the earth looks like a distributed ellipse, and same with Jupiter. The eccentricity of the earth is variable because of Jupiter


