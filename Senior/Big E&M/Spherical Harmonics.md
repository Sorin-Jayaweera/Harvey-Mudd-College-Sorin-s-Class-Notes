
Take spherical coordinates $r,\theta,\phi$.

We have the green's function
$$
\begin{align}
G = \frac{1}{\left| \vec{x}-\vec{x}' \right| } + F(x,x')
\end{align}
$$

We are trying to solve
$$
\begin{align}
\nabla^{2}\phi = -4\pi \rho
\end{align}
$$
The arbitrary $F$ has to still satisfy spherical coordinates $\vec{\nabla}^{2}F=0$

We can solve $\vec{\nabla}^{2}F=0$ with separation of variables. The general solution of $F$ is 
$$
\begin{align}
F = \sum_{0}^{\infty} \sum_{m=-l}^{l} (A_{lm}r^{l}+ B_{lm} r^{-(l+1)}  ) Y_{lm}(\theta,\phi) 
\end{align}
$$
These are the spherical harmonics. $A_{lm}\text{ and } B_{lm}$ are determined from boundary conditions.

They are all orthonormal. They are related to LeGendre functions as
$$
\begin{align}
Y_{lm}(\theta,\phi) = \sqrt[]{ \frac{(2l+1)}{4\pi} \frac{(l-m)!}{(l+m)!} } \underbrace{ P^{m}_{l} }_{ \text{Associated Legendre Polynomials } } \cos\theta e^{im\phi}  
\end{align}
$$

where
$$
\begin{align}
P^{m=0}_{l} \cos\theta = \underbrace{ P_{l} }_{ \text{ Legendre Polynomial } }\cos\theta  
\end{align}
$$

We have a few of these finite polynomials.
$$
\begin{align}
P_{0}(x) = 1 \\
P_{1}(x) = x \\
P_{2}(x) = \frac{1}{2}(3x^{2}-1)   
\end{align}
$$

$$
\begin{align}
\int_{-1}^{1} P_{l'}(x)P_{l}(x)dx = \frac{2}{2l+1} \delta(l,l') 
\end{align}
$$
We see that these orthogonal (not orthonormal though)
$$
\begin{align}
\iint Y^{*}_{l'm'} (\theta ,\phi) Y(\theta,\phi) \sin ^{2}\theta d\theta d\phi = \delta_{l',l} \delta_{m',m}   
\end{align}
$$

We have an identity
$$
\begin{align}
\frac{1}{\left| \vec{x}-\vec{x}' \right| } = \sum_{l=0}^{\infty} \frac{r_{<}^{l}}{r_{>}^{l+1} } P_{l}(\cos \gamma)  
\end{align}
$$
$r_{>}$ and $r_{<}$ are two regimes - when the length of $x$ is greater or less than $x'$. The $r_{<}$ is just smaller of the two, and $r_{>}$ is the larger of the two. $\gamma$ is the angle between $\vec{x}$ and $\vec{x}'$. 

## Example
Lets solve a problem using all of this. Anyone in basic E&M would have a heart attack and fall immediately. 

lets take a loop with uniformly distributed charge $Q$ over a radius $a$. The $\hat{z}$ axis goes through the center of the loop (which is along the $\hat{x}-\hat{y}$ plane). 
![[20260929_095954.jpg]]
The origin is a distance $b$ below the center of the circle. The distance from any point on the ring to the origin is $c = \sqrt[]{ a^{2}+b^{2} }$. Find the potential everywhere. 

Everywhere except for at the ring we have $\vec{\nabla}^{2}\phi=0$.

We can write $\phi$ as a sum of spherical harmonics, valid everywhere except for the ring. We just need to find $A_{lm}\text{ and } B_{lm}$. We have symmetry around the $\hat{z}$ axis, so we don't have any $\varphi$ (angle) dependence. 

Lets find the potential everywhere on the $\hat{z}$ axis. Lets draw $\vec{x}'$ as a bit of charge on the ring. The distance from the bit of charge on the ring to point on the $\hat{z}$ axis has the vector $\vec{x}-\vec{x}'$. As we add by superposition, the distance from point charge to observation stays the same. The potential at the point is just $\phi(x=0,y=0) = \frac{Q}{\left| \vec{x}-\vec{x}' \right|}$.

Lets see if evaluating on the $\hat{z}$ axis is enough to determine the $A_{lm},B_{lm}$ for us to use everywhere. $\left| \vec{x}' \right|=c$.


We can use the formula involving $x_{>}$ and $x_{<}$. 

Along the $\hat{z}$ axis, we have
$$
\begin{align}
\phi(z) = Q \sum_{l=0}^{\infty} \begin{cases}
 \frac{z^{l}}{c^{l+1}} P_{l}\cos(\alpha) & z<c,  & r_{<} =z \\
\frac{c^{l}}{z^{l+1}}P_{l}\cos \alpha & z>c,  & r_{<} = c 
\end{cases}
\end{align}
$$
We have taken the nice function and written it in the most horrific way possible.
$$
\begin{align}
\frac{Q}{\left| \vec{x}-\vec{x}' \right| }=Q \sum_{l=0}^{\infty} \begin{cases}
 \frac{z^{l}}{c^{l+1}} P_{l}\cos(\alpha) & z<c,  & r_{<} =z \\
\frac{c^{l}}{z^{l+1}}P_{l}\cos \alpha & z>c,  & r_{<} = c 
\end{cases}
\end{align}
$$
Lets now try to write $\phi$ off the $z$ axis. 

We have no $\varphi$ dependence, so 
$$
\begin{align}
A_{lm} = B_{lm} \text{ if } m \neq  0  
\end{align}
$$

With spherical harmonics,
$$
\begin{align}
\phi = \sum_{l=0}^{\infty} \sum_{l=-l}^{l} (A_{lm}r^{l}+ B_{lm}r^{-(l+1)}) \underbrace{ Y_{lm}(\theta,\varphi) }_{ e^{im\varphi} } \\
= \sum_{l=0}^{\infty} (A_{l}r^{l} + B_{l} r^{-(l+1)} )P_{l}\cos\theta \sqrt[]{ \frac{2l+1}{4\pi} }   
\end{align}
$$
Notice that $z^{l+1}$ looks like $B_{l}r^{-(l+1)}$, and $z^{l}$ looks like $A_{lm}r^{l}$.

$$
\begin{align}
Q \sum_{l=0}^{\infty} \frac{r_{<}^{l} }{r_{>}^{l+1} } P_{l}(\cos \alpha) P_{l}(\cos\theta)  
\end{align}
$$

We can map to the general solution. On the $\hat{z}$ axis, if for $z < c$ we have $A_{l}= \frac{Q}{c^{l+1}}P_{l}(\cos \alpha)$ and $B_{l}=0$. We replace $A_{l}$ with $\frac{Q}{c^{l+1}}$, $P_{l}\cos\theta=1$, and we get the expression for $z<c$. 

If we have $z>c$, $A_{l}=0$, $B_{l}=c^{l}Q P_{l}(\cos \alpha)$. We then have the $z>c$ condition. 

We are evaluating on the $\hat{Z}$ axis, $\theta=0$, and $z$ is the radial distance from the origin $r$. $r=z,\theta=0$.
$$
\begin{align}
\phi = \sum_{l}^{} (A_{l}z^{l}+ B_{l}z^{-(l+1)}  ) \sqrt[]{ \frac{2l+1}{4\pi} } 
\end{align}
$$
We compared this with the $z<c$ and $z>c$ condition, which gives us the constants $A_{l}\text{ and } B_{l}$. Combining the two into one equation is what gave us
$$
\begin{align}
\sum_{l=0}^{\infty} Q P_{l}\cos \alpha \frac{r_{<}^{l} }{r_{>}^{l+1} } P_{l}\cos(\theta)  
\end{align}
$$
$$
\begin{align}
r_{<},r_{>} = \{c,r\}  
\end{align}
$$


## Cylindrical coordinates

Lets take a random corner edge of a triangle with angle $\alpha$ that extends to infinity and is grounded. Lets put a charge $q$ at a coordinate. 
![[20260929_102933.jpg]]

We can use method of images! 

Lets try to put a charge outside the region of interest $-q$ living below the wedge. 
$$
\begin{align}
\phi = \frac{q}{r}+ \underbrace{ \dots }_{ F }
\end{align}
$$
where $r$ is the radius from the point we care about to the charge $q$. ($\vec{x}$ is from the origin (where the two wedge ends meet) to the point we care about, $r$ is from that point we care about to the charge $q$).
We should add another charge $-q$ at the other side of the wedge to fit that boundary condition - but now we have an extra charge and have to cancel it out with yet another charge. Uh oh! We have to recursively add image charges to get a closed loop (which only happens for a discrete set of $\alpha$). This happens when $\alpha= \frac{\pi}{n}$, where $n$ is an even $\mathbb{Z}$. We would have $2n-1$ image charges.

![[20260929_103414.jpg]]

Lets take the case $\alpha=\frac{\pi}{2}$, so it is a right angle wedge.
![[20260929_103429.jpg]]

This works because the $q$ in the bottom left works as a mirror for both $-q$ equally. 

Now lets look at $\frac{\pi}{4}$.
![[20260929_103658.jpg]]


We get 
$$
\begin{align}
\phi= \sum_{i=1}^{2n} \frac{(-1)^{i+1}q}{\sqrt[]{ (R \cos \varphi_{i} - x)^{2} + (R\sin \varphi_{i} -y)^{2} + z^{2} } }
\end{align}
$$

This denominator is constructing the distance from the point charge to the point of interest. $R=(x,y,z)$, and $x,y,z$ are the point of observation that we want to find $\phi$ for. 


Lets make a new version where the diagonal plane has $\phi=\phi_{0}$, and the bottom plane has $\phi=0$. They are not connected at the edge. What happens at the corner of separate potentials? 

$$
\begin{align}
\phi(r,\varphi,z)
\end{align}
$$
$$
\begin{align}
\vec{\nabla}^{2} \phi = 0  \\
= r \frac{ \partial  }{ \partial r } \left( r \frac{ \partial  }{ \partial r }  \right)\phi + \frac{ \partial^{2} }{ \partial \varphi^{2} } \phi
\end{align}
$$
This is like "particle in a cylindrical box". Same principle, different spatial functions. 

We write
$$
\begin{align}
\phi = R(r)\Phi(\phi) & \text{ (no z dependence) }
\end{align}
$$
We get
$$
\begin{align}
0 = r \frac{ \partial  }{ \partial r } \left( r \frac{ \partial  }{ \partial r }  R \Phi\right) + \frac{ \partial^{2} }{ \partial \varphi^{2} } (R\Phi)
\end{align}
$$
We can bring out $\Phi$, so we get
$$
\begin{align}
\Phi r \frac{ d }{d r } \left( r \frac{ d R(r)}{d r }  \right) + R \frac{ d ^{2}\Phi(\varphi)}{d \varphi^{2} } 
\end{align}
$$

We divide by $R\Phi$, and get
$$
\begin{align}
0=\frac{1}{R} r \frac{ d }{d r } \left( r \frac{ d R}{d r }  \right) + \frac{1}{\Phi} \frac{ d ^{2}\Phi}{d \varphi^{2} } 
\end{align}
$$
These must be constant and opposite each other. At one end we'll get oscillations of cos and sin. Physically, let's set $\Phi$ to have that.

$$
\begin{align}
-\nu^{2}  & \equiv  \frac{1}{\Phi} \frac{ d ^{2}\Phi}{d \varphi^{2} }  \\
+ \nu^{2} &  \equiv  \frac{1}{R} r \frac{ d }{d r } \left( r \frac{ d R}{d r }  \right)
\end{align}
$$
--- 
New day so lets start earlier

$$
\begin{align}
\phi = R(r)\Phi(\varphi) \\
\nabla^{2} \phi = \frac{1}{r} \frac{ \partial  }{ \partial r } \left( \frac{r \partial (R(r)\Phi(\varphi))}{\partial r} \right) + \frac{1}{r^{2}} \frac{ \partial^{2} }{ \partial \varphi^{2} } (R(r)\Phi(\varphi)) = 0 \\
\frac{1}{Rr} \frac{ d }{d r } \left( r \frac{ d R}{d r }  \right) + \frac{1}{r^{2}\Phi} \frac{ \partial^{2}\Phi }{ \partial \varphi^{2} } = 0 \\
\frac{r}{R}\frac{ d }{d r } \left( r \frac{ d R}{d r }  \right) + \frac{1}{\Phi} \frac{ d ^{2}\Phi}{d \varphi^{2} } =0
\end{align}
$$
Lets call the left $r$ dependence $+\nu^{2}$, and the right $\varphi$ dependence $-\nu^{2}$. We have two equations

$$
\begin{align}
\frac{ d ^{2} \Phi}{d \varphi^{2} }  & = -\nu^{2} \Phi \\
\frac{r}{R} \frac{ d }{d r } \left( r \frac{ d R}{d r }  \right) & = \nu^{2} 
\end{align}
$$

For the $\Phi$ function, we have $\Phi(\varphi)= A_{\nu}\cos(\nu \varphi)+ B_{\nu}\sin(\nu \varphi)= a_{\nu}\sin(\nu \varphi+\alpha_{v})$
for $\nu = n \in \mathbb{Z}$

For the $R$ function, we guess at a series solution ( it looks like the series expansion for $e^{x}$)
$$
\begin{align}
R(r) = \sum_{n}^{} c_{n} r^{n} \\
r \frac{ d }{d r } \left( \sum_{n}^{} a_{n} nr^{n}\right) = \nu^{2} \sum_{n}^{} a_{n} r^{n} \\
\sum_{n}^{} a_{n}n^{2}r^{n}= \nu^{2} \sum_{n}^{} a_{n} r^{n} \\
n = \pm \nu 
\end{align}
$$
The solutions we have take the form
$$
\begin{align}
R(r)  & = c_{\nu}r^{\nu}+ c_{-\nu} r^{-\nu}  \\
\phi  & = \sum_{n=1}^{\infty} a_{n} r^{n}\sin(n\varphi+\alpha_{n} ) + \sum_{n=1}^{\infty} b_{n} r^{-n}\sin(n\varphi+ \beta n )
\end{align}
$$
(again, $\phi$ is the potential and not the separated variable function $\Phi$ or the dependence $\varphi$)

Lets treat the $n=0$ case specially, which has $+a_{0} + b_{0} \ln(r)$ because
$$
\begin{align}
\cancelto{  }{ \frac{r}{R} } \frac{ d }{d r } \left( r \frac{ d r}{d R }  \right) = 0 \implies r \frac{ d R}{d r } = C \implies \frac{ d R}{d r } = \frac{C}{r} \\
\implies R(r) = C \ln (r)+c'
\end{align}
$$



We can make things nice with boundary conditions. We want $\phi$ to be finite as $r\to 0$, so we can just cross out the $b_{0}\ln r$ term and the $\sum_{n=1}^{\infty}b_{n}r^{-n}\sin(n\varphi+\beta n)$ term. 

We also have
$\phi(\varphi=0)=0$. That gets rid of the $+\alpha_{n}$ in the sin term. 

Finally, we have $\phi (\varphi= \alpha)=\phi_{0}$. This tells us that
$\phi =  \sum_{n=1}^{\infty}a_{n}r^{n}\sin(nx)+ a_{0}=\phi_{0}$

Oof, we find that this is not solvable because we can't have $a_{0}=0$. Lets go back and do surgery.


$\nu$ NOT an integer, but restricted to $0 < \varphi < \alpha$.

We change $n$ back to $\nu$
$$
\begin{align}
R(r) = c_{\nu} r^{\nu} + c_{-\nu} r^{-\nu} \\
\phi = \sum_{\nu >0}^{} a_{\nu} r^{\nu}\sin(\nu \varphi + \cancelto{  }{ \alpha_{\nu} } )
\end{align}
$$
We need $a_{0}=0$. We are left only with $B_{\nu}$ from $A_{\nu}\cos(\nu \varphi)+ B_{\nu}\sin(\nu \phi)$ as an unknown. We have 

$$
\begin{align}
\phi(\alpha) = \sum_{n>0}^{} B_{\nu} r^{\nu} \sin (\nu \alpha)=\phi_{0}
\end{align}
$$
(the alpha is $\varphi$ evaluated at $\alpha$). This sets the condition that 
$\nu = \frac{\pi n}{\alpha}$

We don't have the single value solution, so we don't have a series solution. We have a discrete, but shifted over some fraction (i assumed it would just be an integral, but that won't work with the boundary condition for $\alpha$ that we saw above).

aha! if we have $\nu=0$, we have a linear term $c_{0}\varphi$ (because we have second derivative is constant). We need to add that in, so

$$
\begin{align}
\phi(r,\varphi) = \sum_{m=1}^{\infty} a_{m} r^{\frac{m\pi}{\alpha}}\sin\left( \frac{m\pi \varphi}{\alpha} \right) + \frac{\phi_{0}(\varphi)}{\alpha}
\end{align}
$$
This is the solution! This is definitely not single valued? 

There is still an ambiguity. $a_{m}$ is not determined, because we don't have a limit at $\infty$. 

In the case that $r$ is small, we can find something. The powers are successively smaller, so we can keep just the leading order term as the best solution.

$$
\begin{align}
\phi(r=0) = \frac{\phi_{0}}{\alpha} + a_{n} r^\frac{\pi}{\alpha}
\end{align}
$$
There is a coordinate singularity, since $\phi$ doesn't exist at $r=0$. We have to switch to cartesian coordinates. We find the electric field approaches $0$, so there are no surface charges. $\sigma\to 0$ at the corner. 



