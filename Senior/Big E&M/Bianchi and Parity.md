
$$
\begin{align}
E^{i}= F_{i,0} 
\end{align}
$$


$j^{\mu}= (pc,\vec{j})$



$$
\begin{align} \\
\underbrace{ F_{0i} }_{ -E^{i} }= \partial_{0} A_{i} - \partial _{i} A_{0}  \\
-\vec{E} = \frac{1}{c} \frac{ \partial \vec{A} }{ \partial t } + \vec{\nabla} \phi\\
\vec{E} = -\vec{\nabla} \phi - \frac{1}{c} \frac{ \partial \vec{A} }{ \partial t } 
\end{align}
$$
where
$$
\begin{align}
A_{0} = -\phi 
\end{align}
$$

We can take this to write out 

$$
\begin{align}
\underbrace{ F_{0i} }_{ -E^{i} }= \partial_{0} A_{i} - \partial _{i} A_{0} \\
\implies F_{ij} = \partial _{i}A_{j} - \partial _{j}A_{i}  \\
\implies [\vec{B} = \vec{\nabla}\times \vec{A}] \\
A_{0} \to   A_{0} + \partial_{0} \Lambda \\
\phi \to   \phi - \frac{1}{c} \frac{ \partial \Lambda }{ \partial t }  \\
\vec{A} \to   \vec{A} + \vec{\nabla}\Lambda
\end{align}
$$



Lets take a couplet set of equations, where E and B appear in both as $F^{\mu \nu}$. We normally solve this computationally, but we can set one of these and solve for the other. In most cases the feedback between these two is minimal (i.e. in charged plasma fluid dynamics its critical to have the back reaction).

$$
\begin{align}
\partial_{\mu} F^{\mu \nu}  & = - \frac{4\pi}{c}j ^{\nu} \to   \vec{E},\vec{B} \\
\dot{P}_{\mu}  & = q F_{\mu \nu} u^{\nu} \to   x^{\nu}(\tau) \\
\partial_{\nu} j^{\nu} & =0
\end{align}
$$
Lets try to find $E$ and $B$ given charges $x^{\nu}(\tau)$.



Lets look at Maxwell's in their full glory in vector form
$$
\begin{align}
\vec{\nabla}\cdot \vec{E} = 4\pi \rho \\
\vec{\nabla}\cdot \vec{B}  0 \\
\vec{\nabla}\times \vec{E} + \frac{1}{c} \frac{ \partial \vec{B} }{ \partial t } = 0 \\
\vec{\nabla} \times \vec{B} - \frac{1}{c } \frac{ \partial \vec{E} }{ \partial t } = \frac{4\pi}{c}\vec{j}
\end{align}
$$
We have 6 fields - three components in $\vec{E}$ and $\vec{B}$ each, all depending on time and space. This is a $2^{nd}$ order PDE for $\vec{E}(t,\vec{x}),\vec{B}(t,\vec{x})$.

We have the Existence-Uniqueness theorem. These equations have a solution if we give boundary conditions. 

Existence = boundary conditions
Uniqueness = any solution with boundary conditions is the ONLY solutions (unique).

We need to know $\rho, \vec{J}$, and boundary conditions (a region of space where we find $\vec{E}$ and $\vec{B}$ in a volume is determined by $\rho,\vec{J}$ inside the volume and the $\vec{E}$ and $\vec{B}$ at the boundary). We can start with this as static, zero time dynamics. 



# problem
Lets take a point charge exactly at $(0,0,0)$ with no motion
$$
\begin{align}
\vec{J}=0 \\
\rho = q \delta^{3}(\vec{x})
\end{align}
$$
This is a delta function for when $\vec{x}=(0,0,0)$.

The delta function only makes sense in an integral,
$$
\begin{align}
\int_{-\infty}^{\infty} dx f(x) \delta(x-a) \equiv  f(a) \\
\end{align}
$$

### Lets find some identities for the $\delta$ function

$$
\begin{align}
\int_{-\infty}^{\infty} f(x) \frac{ d \delta(x-a)}{d x } dx  & = \int_{-\infty}^{\infty} \frac{ d }{d x } (f(x)\delta(x-a)) dx - \int_{-\infty}^{\infty} \frac{ d f}{d x } \delta(x-a) \\
 & = f(\infty)\cancelto{  }{ \delta(\infty-a) }- f(-\infty)\cancelto{  }{ \delta(-\infty-a) } - \frac{ d f}{d x } (a)
\end{align}
$$
if $a$ is finite, these vanish


so,
$$
\begin{align}
\int_{-\infty}^{\infty} dx f(x)\delta'(x-a)= -f'(a)
\end{align}
$$


What about $\delta(f(x))$
We have from Taylor expanding $f(x)$ around it's zeros,
$$
\begin{align}
\delta(f(x)) = \sum_{i}^{} \frac{\delta(x-\underbrace{ x_{i} }_{ \text{ zeros } } )}{\left| \frac{ d f}{d x } (\xi i) \right| }
\end{align}
$$


$$
\begin{align}
\delta^{D}(\vec{x}-\vec{a}) & = \delta(x^{0}-a^{0})\delta(x^{1}-a^{1})\dots \\
\delta^{4}  & = \delta(x^{0}-a^{0})\delta^{3}(\vec{x}-\vec{a})
\end{align}
$$
also
$$
\begin{align}
\delta^{D}(C_{\mu \nu} (x^{\nu}-a^{\nu}))= \frac{\delta^{D}(x-a)}{\left| \det{(C)}  \right| }
\end{align}
$$


Assuming one zero of $f$ at $a^{\mu}$,
$$
\begin{align}
\delta^{D}(\underbrace{ f(x) }_{ f^{\mu}(x^{0},x^{1},x^{2},\dots) }) = \frac{\delta^{D}(x-a)}{\left| \det{( \delta_{\mu} f^{\nu}(a) )}  \right| }
\end{align}
$$
We have a representation of $\delta$
$$
\begin{align}
\begin{pmatrix}
\delta_{0} f^{0} & \delta_{0}f^{1} & \delta_{0}f^{2} \\
\delta_{1} f^{0} & \delta_{0}f^{1} & \dots \\
\vdots
\end{pmatrix}
\end{align}
$$

So we have the representation of $\delta$
$$
\begin{align}
\delta(x) = \lim_{ \sigma \to 0 } \frac{1}{\sqrt[]{ \pi } \sigma}e^{-\frac{x^{2}}{\sigma^{2}}}
\end{align}
$$

## Back to the problem

No motion. 
We have
$$
\begin{align}
\vec{\nabla}\cdot \vec{E} = 4\pi \rho == 4\pi q \delta^{3}(x) \\
\vec{\nabla}\cdot \vec{B}=0 \\
\vec{\nabla}\times \vec{E} + \frac{1}{c} \frac{ d B}{d t } = 0 \\
\vec{\nabla}\times \vec{B} - \frac{1}{c} \frac{ \partial \vec{E} }{ \partial t } = 0
\end{align}
$$

Lets take the assumption that $\vec{E},\vec{B}\to 0$ at $\infty$.

We have no motion, so toss the derivatives. Therefore, $\nabla \times \vec{B} = 0$ and $\nabla\cdot \vec{B} = 0$. $B = 0$

We are left only with
$$
\begin{align}
\vec{\nabla} \cdot \vec{E} = 4\pi q \delta^{3}(x), \vec{\nabla}\times \vec{E}  = 0 \\
\end{align}
$$
Lets take a guess
$$
\begin{align}
\vec{E} = \frac{q\vec{x}}{\left| \vec{x} \right| ^{3}}
\end{align}
$$
This attenuates by $\frac{1}{x^{2}}$.

Lets check the relation (although its not differentiable at $x=0$). We can take the divergence of $E$ and integrate it over a function to recover the delta function.

We need to show that
$$
\begin{align}
(\vec{\nabla} \cdot \vec{E})f(x) dVol = 4\pi q f(0)
\end{align}
$$
for any arbitrary $f$.


$$
\begin{align}
\int \partial _{i} \left( \frac{qx^{i}}{\left| \vec{x} \right| ^{3}} \right) f(x)dVol 
\end{align}
$$
Lets move the derivative because we don't know how to differentiate $\frac{1}{x^{3}}$ at $0$.

$$
\begin{align}
= - \int_{}^{} \frac{qx^{i}}{\left| \vec{x} \right|^{3} } \partial _{i}f(x)dVol + \cancelto{ \text{ because vanish at infinity } }{ \int \partial _{i} \left( \frac{qx^{i}}{\left| x \right| ^{3}}f(x) \right) dVol }
\end{align}
$$
Lets replace the integral with one over all of space except a tiny spherical region around the origin, of radius $\epsilon$. Now in the integral we don't have the singularity, we've punted the singularity to when we evaluate the limit. 


Lets take
$$
\begin{align}
=\lim_{ \epsilon \to 0 } - \int_{\text{ excluding } \epsilon}  \frac{qx^{i}}{\left| x \right| ^{3}} \partial _{i} f(x) dVol \\
= \lim_{ \epsilon \to 0 } \int_{\text{ not  }\epsilon} \left( -\delta _{i} \frac{qx^{i}}{\left| x \right| ^{3}}f(x) + \partial _{i} \left(  \frac{qx^{i}}{\left| x \right| ^{3}} \right)f(x) \right) dVol
\end{align}
$$
We can take both derivatives. Lets use the divergence theorem for the first term.
$$
\begin{align}
\lim_{ \epsilon \to 0 } \int_{\text{ not } \epsilon} (-\delta _{i}) \left( \frac{qx^{i}}{\left| x \right|^{3} }f(x) \right) dVol = \lim_{ \delta \to 0 } - \oint \frac{qx^{i}}{\left| x \right| ^{3}}f(x) dA_{i}
\end{align}
$$
$dA_{i}$ points outwards, but our $\hat{A}$ is radially inwards (why??)

$$
\begin{align}
\lim_{ \delta \to 0 } \frac{q}{\left| \vec{x} \right|^{2} }f(0)4\pi\epsilon^{2} \\
\lim_{ \delta \to 0 } \frac{q}{\epsilon^{2} }f(0)4\pi\epsilon^{2} \\
= 4\pi q f(0)
\end{align}
$$

Now lets look at the other side (it better be zero)

$$
\begin{align}
\partial _{j} \left(  \frac{x^{i}}{\left| \vec{x} \right| ^{3}} \right) = \frac{\delta^{i}_{j} }{\left| \vec{x} \right| ^{3}} + x^{i} \left( -\frac{3}{2} \right) \frac{2x^{j}}{\left| \vec{x} \right| ^{5}} \\
= \frac{\partial^{i}_{j} }{\left| x \right| ^{3}} - 3 \frac{x^{i}x^{j}}{\left| x \right| ^{5}} \\
\delta _{i} \left( \frac{\xi i}{\left| \vec{x} \right| ^{3}} \right) = \frac{\delta^{i}_{i}}{\left| \vec{x} \right| ^{3}} - 3 \frac{x^{i}x^{i}}{\left| \vec{x} \right| ^{5}}
\end{align}
$$
