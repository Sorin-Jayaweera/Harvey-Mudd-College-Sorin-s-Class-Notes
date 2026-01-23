Some notes ahead of time
## Pre notes
From differential equations, the reader should know the following:
### Solving Homogenous ode:
$$
\begin{align}
\ddot{x}_{n} + 2\beta \dot{x}_{n} +\omega_{0}^{2}x_{n} =0 
\end{align}
$$
Finding a particular solution $x_{p}$
$$
\begin{align}
\ddot{x}_{p} +2 \beta \dot{x} _{p} +\omega^{2}_{0} x_{p} = \frac{F_{\text{ drive }}(t)}{m}
\end{align}
$$
The general solution is
$$
\begin{align}
x(t)= x_{n} (t)+x_{p} (t)
\end{align}
$$


### Homogenous solution
We have underdamped, overdamped, and critically damped systems.

$$
\begin{align}
x(t) = \begin{cases}
e^{-\beta t}C\cos[\sqrt[]{ \omega_{0}^{2} - \beta^{2}} t + \delta ], &  \beta< \omega_{0}  \text{ Underdamped } \\
Ae^{-(\beta+ \sqrt[]{ \beta^{2}-\omega_{0}^{2} } )t}+ Be^{-(\beta- \sqrt[]{ \beta^{2}\omega_{0}^{2} } )t}, &  \beta> \omega_{0} \text{ Overdamped } \\
Ae^{-\beta t}+Bte^{-bt},  & \beta= \omega_{0} \text{ Critically Damped }
\end{cases}
\end{align}
$$


All of these damp to zero for $\beta t \gg 1$


## Damped Driven Oscillators

![[Pasted image 20251027144834.png|500]]

Lets let there be some amount of friction
$$
\begin{align}
\vec{F}_{\text{ friction }} = -b\vec{v}
\end{align}
$$
We can't do Lagrangian mechanics. This is painful. Lets use regular Newtonian mechanics. Draw a free body diagram with friction opposing motion and a net spring constant back towards equilibrium.

Lets add some external driving to make it fun: Lets drive the left wall as a function of time with $\vec{F}_{\text{ drive }}(t)$. 
The force from the driven wall will transmute through the springs.

$$
\begin{align}
m \ddot{x}= -b\dot{x}-kx-k'x+F_{\text{ drive }}  \\
\end{align}
$$

We can rewrite this
$$
\begin{align}
\ddot{x} = -\underbrace{ \frac{b}{m} }_{ \text{ 2 }\beta }\dot{x}- \underbrace{ \frac{k+k'}{m} }_{ \omega_{0}^{2} }x + \frac{F_{\text{ drive }}}{m}
\end{align}
$$
$\beta \text{ and }  \omega_{0}$ have dimensions of frequency, $\frac{1}{\text{ time }},s^{-1}$.

For now, lets take a very special $F_{\text{ drive }}(t)$ to make it easy to solve, and then we can make it general.
Let $F_{\text{ drive }}(t)=f_{0}\cos(\omega t)$.

The system is
$$
\begin{align}
\ddot{x}+2\beta\dot{x} + \omega_{0}^{2}x = f_{0}\cos(\omega t)  \\
\end{align}
$$
Lets make this COMPLEX.
$$
\begin{align}
\ddot{z} + 2\beta \dot{z} + \omega_{0}^{2}z=f_{0}e^{i\omega t}
\end{align}
$$
Where our solution is just $\ce{ Re }[z(t)]$

We make the Ansatz $z(t)=Ae^{i\omega t}=\left| A \right|e^{i(\omega t+\delta)}$, where $A=\left| A \right|e^{i\delta}$.

Lets use this solution in the differential equation.
$$
\begin{align}
-\omega^{2}Ae^{i\omega t} + 2\beta(i\omega)Ae^{i\omega t}+\omega_{0}^{2}Ae^{i\omega t}=f_{0}e^{i\omega t}
\end{align}
$$
We get now
$$
\begin{align}
A(\omega_{0}^{2}-\omega^{2}+2i \beta\omega)=f_{0} \\
A = \frac{f_{0}}{(\omega_{0}^{2}-\omega^{2})+2i \beta \omega} 
\end{align}
$$
This has a magnitude $\left| A \right|$ and phase $\delta$. This is just some complex number. Lets take that solution to get the amplitude and phase information. 
How do we solve for $\delta$?
We can write $A$ as real and imaginary.
$$
\begin{align}
\text{ let }A = a+ib
\end{align}
$$
$$
\begin{align}
a = \ce{ Re }(A), b= \ce{ Im  }(A)
\end{align}
$$
$$
\begin{align}
\tan\delta = \frac{\pu{ Im}(A)}{\pu{ Re}(A)}
\end{align}
$$
We can simplify by multiplying $A$ by $\frac{[(\omega_{0}^{2}-\omega^{2})-2i \beta \omega]}{[(\omega_{0}^{2}-\omega^{2})-2i \beta \omega]}$. This is just $1$, but will give us a nice real and imaginary part. 
$$
\begin{align}
A = \frac{f_{0}(\omega_{0}^{2}-\omega^{2})}{(\omega_{0}^{2}-\omega^{2})^{2}+4\beta^{2}\omega^{2}} + i\frac{f_{0}(-2\beta \omega f_{0} )}{(\omega_{0}^{2}-\omega^{2})^{2}+4\beta^{2}\omega^{2}}
\end{align}
$$


$$
\begin{align}
\left| A \right| = \sqrt[]{ a^{2}+b^{2} } 
\end{align}
$$
Lets take these monstrosities. 

$$
\begin{align}
\sqrt[]{ \frac{f_{0}^{2}(\omega_{0}^{2}-\omega^{2})^{2} + 4\beta^{2}\omega^{2}f_{0}^{2}}{[(\omega_{0}^{2}-\omega^{2})^{2}+4\beta^{2}\omega^{2}]^{2}} } 
\end{align}
$$
This simplifies nicely
$$
\begin{align}
\left| A \right| =\frac{f_{0}^{2}}{\sqrt[]{ (\omega_{0}^{2} -\omega^{2})^{2}+4\beta^{2}\omega^{2} }}
\end{align}
$$
We also have
$$
\begin{align}
\tan\delta  & = \frac{\pu{ Im}(A)}{\pu{ Re}(A)} \\
 & =\frac{(-2\beta \omega f_{0})}{f_{0}(\omega_{0}^{2}-\omega^{2})} \\
= \frac{2 \beta \omega}{(\omega_{0}^{2}-\omega^{2})^{2}}
\end{align}
$$

We find the quadrant from here

Note that this has no free parameters.
$$
\begin{align}
z(t)_{p}  = \left| A \right| e^{i(\omega t+\delta)}
\end{align}
$$
Where the amplitude and phase only depend on system parameters.

This is the particular solution that the system converges to over time, we will decay to exactly this. 

Amplitude:

At $\omega=\omega_{0}$, we'll have $A= \frac{f_{0}}{2\beta \omega}$. For large mismatch between $\omega \text{ and } \omega_{0}$, we'll have $A=\frac{f_{0}}{\sqrt[]{ \omega^{4}+4 \beta^{2}\omega^{2} }}$

For $\omega_{0}$ to be in resonance, we need
$$
\begin{align}
(\omega_{0}^{2}-\omega^{2})^{2} \leq 4\beta^{2}\omega^{2} \\
\left| \omega_{0}^{2}-\omega^{2} \right| \leq 2\beta \omega \\
(\omega_{0}+\omega)\left| \omega_{0}-\omega \right| \leq 2\beta \omega  
\end{align}
$$
Because we want $\omega_{0}\approx \omega$, this becomes
$$
\begin{align}
\left| \omega_{0}-\omega \right| \leq \beta
\end{align}
$$
This is the width of resonance where we'll get a big boost. 
![[Pasted image 20251027155440.png]]
As $\beta$ goes to zero, we have no damping and infinite response. We no longer have the approximation of $U_{\text{ sho }}=\frac{1}{2}kx^{2}$, and get nonlinear dynamics. Friction makes life nicer.


## General Driving

We can represent any periodic 
$$
\begin{align}
F_{\text{ drive }}(t)=\ce{ Re}\left[ \sum_{j}^{} A_{j} e^{i\omega_{j} t} \right]
\end{align}
$$
Only one term will have $\omega_{j}=\omega_{0}$: Where driving will match the natural frequency. We can generally ignore any frequency components that don't match the natural frequency.