## Recap:
Lets start by talking about the overall process for particle in a box. Everything we do for a finite square well will follow the same process.

There is a potential energy function $V(x)$ defined that bounds a nonrelativistic particle.

$$
\begin{align}
V(x) = \begin{cases}
0 & -\frac{a}{2} < x < \frac{a}{2} \\
v_{0} & \text{ otherwise }
\end{cases}
\end{align}
$$
We write out the time independent Schrödinger equation in each region, and solve for $\psi_{n}$, defining a parameter ($k$) that relates to $E$
We can choose $\sin \text{ and } \cos, \text{ or } e^{ikx}$.

We then apply boundary conditions to restrict the values of energy.

Finally, we use the energy eigenstates to decompose the wave function. 
$$
\begin{align}
\Psi(x,t)=\sum_{n}^{} c_{n}(0)\psi_{n}(x)e^{-i \frac{E_{n}}{\hbar}t}
\end{align}
$$
## Finite square well:

We see that solutions are either even or odd for the infinite square well, where we can fit either a sin or a cos (since we are centered at the origin, so we care that the value in the center is either 1,-1,0).

With a finite well, we decay the wave function past the boundaries, since it is now possible to pass the edges of the well.

At the boundary we have to set that the first derivatives are continuous, not just the value. We also have to have the function be normalizable, so as $x\to \pm\infty$, this function has to go to $0$.

We define our energy in three regions, above(III) in(II) and below(I) the well.

In the well, we have the standard expression:
$$
\begin{align}
-\frac{\hbar^{2}}{2m} \frac{ \partial^{2} }{ \partial x^{2} } \Psi +0 = E\psi \\
\frac{ \partial^{2} }{ \partial x^{2} } \psi= -\underbrace{ \frac{2mE}{\hbar^{2}} }_{ k^{2} } \psi
\end{align}
$$
For the regions above and below (I and III)
$$
\begin{align}
-\frac{\hbar^{2}}{2m}\frac{ \partial^{2} }{ \partial x^{2} } \psi+v_{0}\psi=E\psi \\
\frac{ \partial^{2} }{ \partial x^{2} } \psi= \underbrace{ \frac{2m(v_{0}-E)}{\hbar^{2}} }_{ \kappa^{2} }\psi
\end{align}
$$

Inside the square well we have
$$
\begin{align}
k=\sqrt{ \frac{2mE}{\hbar^{2}} } \\
\kappa= \sqrt{ \frac{2m(v_{0}-E)}{\hbar^{2}} } 
\end{align}
$$
To satisfy the property where the second derivative of a function yields itself, we have the hyperbolic trig solutions and complex exponentials.

$$
\begin{align}
\psi(x)= \begin{cases}
c_{1}e^{\kappa x}+c_{2}e^{-\kappa x}, I \\
Ae^{ikx}+ Be^{-ikx}, II \\
D_{1}e^{\kappa x}+D_{2}e^{-\kappa x},III
\end{cases}
\end{align}
$$
Because the function has to go to zero at infinity, we can set $c_{2}=d_{1}=0$, since $e^{kx}\to \infty \text{ as } x\to \infty$ (and we have $-\infty$ for the case below the well).

We can now apply the rest of the boundary conditions to make the functions continuous.

Lets take the first derivative in each region
$$
\begin{align}
\frac{d\psi}{dx}= \begin{cases}
\kappa ce^{\kappa x}  & I \\
ikAe^{ikx} -ikbe^{-ikx} & I I \\
-\kappa d e^{-\kappa x} & I I I \\
\end{cases}
\end{align}
$$
We can start by checking the two continuity equations for regions I and II.
$$
\begin{align}
1) ce^{-\kappa \frac{a}{2}}=Ae^{\frac{-ika}{2}}+Be^{\frac{ika}{2}} \\
2) \kappa ce^{-\kappa \frac{a}{2}}=ikAe^{ikx}-ikBe^{-ikx}
\end{align}
$$
We can multiply 1) by $\kappa$ and set the two right sides equal to each other.

$$
\begin{align}
\kappa Ae^{\frac{-ika}{2}}+\kappa e^{ik \frac{a}{2}}=ikAe^{\frac{-ika}{2}}+Be^{ik \frac{a}{2}}
\end{align}
$$
Lets introduce some lazy notation:
$$
\begin{align}
e^{+}=e^{ik \frac{a}{2}} \\
e^{-}=e^{-ik \frac{a}{2}}
\end{align}
$$

We get
$$
\begin{align}
Ae^{-}(\kappa-ik)=Be^{+}(-ik-\kappa) \\
\end{align}
$$
$$
\boxed{
\begin{align}
\frac{A}{B}=e^{ika} \frac{ik+\kappa}{ik-\kappa}
\end{align}
}
$$
This is a relationship between $A\text{ and } B$.

We have similarly at $x=\frac{a}{2}$

$$
\begin{align}
3) Ae^{\frac{ika}{2}}+Be^{\frac{-ika}{2}}=De^{-\kappa \frac{a}{2}} \\
4) ikAe^{ik \frac{a}{2}} - ikBe^{\frac{-ika}{2}}=-\kappa De^{-\kappa \frac{a}{2}} 
\end{align}
$$

We can do the same process
$$
\begin{align}
\frac{B}{A}=e^{ika} \frac{ik+\kappa}{ik-\kappa}
\end{align}
$$
Apparently, 
$$
\begin{align}
\frac{A}{B}=\frac{B}{A} \\
A=\pm B
\end{align}
$$
We have some consequences of that.

Lets look at $A=B$
Lets take eq 1 and 3, and plug in $A=B$.
$$
\begin{align}
Ce^{\kappa a/2}=Ae^{-}+Ae^{+} \\
De^{-\kappa a/2}=Ae^{+}+Ae^{-}
\end{align}
$$
This tells us $C=D$

If we do this for $A=-B, \implies C=-D$

If A = B, then our equation in the center of the well looks like cos
$$
\begin{align}
\psi_{I I}=2iA\cos kx \\
\end{align}
$$
If $A=-B$, we get
$$
\begin{align}
\psi_{I I}=2iA\sin kx
\end{align}
$$
We still have to find a relationship between $C\text{ and } A$, but it follows by more manipulation of making the function $C_{1} \text{ continuous }$. But, more interesting right now - is energy quantized?

Lets take the case $A=B$
$$
\begin{align}
\kappa Ae^{-}+\kappa Ae^{+}=ikAe^{-}-ikAe^{+} \\
2\kappa A\cos\left( \frac{ka}{2} \right)=ikA\left( -2i\sin\left( \frac{ka}{2} \right) \right) \\
\frac{\kappa}{k}=\tan\left( \frac{ka}{2} \right)
\end{align}
$$
Woah! Only K values that meet this restriction are allowed. This is for the even solutions.

If we do this for the odd solutions,
$$
\begin{align}
\frac{\kappa}{k}=-\cot\left( \frac{ka}{2} \right)
\end{align}
$$
We define 
$$
\begin{align}
\xi=\frac{ka}{2} ~ ~ &  \text{ dimensionless k related to energy } \\
\xi_{0}=\frac{a}{\hbar}\sqrt{ \frac{mV_{0}}{2} }~ ~  & \text{ determinded by V(x)  } \\
 & \text{ for bigger energy wells }
\end{align}
$$



We get the two $\frac{\kappa}{k}$ relations to imply

$$
\boxed{
\begin{align}
\text{( even) } & \tan \xi = \frac{\sqrt{ \xi_{0}^{2}-\xi^{2} }}{\xi} \\
\text{ (odd )} & -\cot \xi=\frac{\sqrt{ \xi_{0}^{2}-\xi^{2} }}{\xi}
\end{align}
}
$$



For the even solutions, we plot $\tan \xi$ and the function.
![[Pasted image 20250207105424.png|300]]
where we have the even and odd functions.
