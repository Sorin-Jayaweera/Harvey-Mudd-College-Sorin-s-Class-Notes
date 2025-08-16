We'll put infinitely tall walls around some region in space and restrict our particle inside it. We say that the particle has a certain amount of energy.

![[Pasted image 20250131101018.png]]

Classically, the particle could be said to have zero energy, but is the the actual lowest amount of energy allowed?

We've localized it to a small location, so we will have some nonzero momentum uncertainty $\delta x\delta p_{x}\geq \frac{\hbar}{2}$

The kinetic energy is written as $E\sim \frac{\left< P_{x} \right>^{2}}{2m}$

$$
\begin{align}
\left< P_{X}^{2} \right> =\Delta P_{x}^{2}+\underbrace{ \left< P_{X} \right> ^{2} }_{ 0 }
\end{align}
$$
This gives us $E\geq \frac{\Delta p_{x}^{2}}{2m}$
We can use $\Delta p_{x}\geq \frac{\hbar}{2l}$ to write our energy as $\frac{\hbar^{2}}{8ml}\neq 0$.

We see that we are not allowed to have 0 energy because we have uncertainty in momentum. The lowest possible energy is at least $\frac{\hbar^{2}}{8ml^{2}}$

We're going to solve the Schrödinger equation so that we can solve it for many different energy functions.


## Separation of Variables

We can propose: $\Psi(x,y)=\psi(x)f(t)$. We say that $\Psi$ is a product of two functions that vary with either x or t. 
This means
$$
\begin{align}
\frac{d}{dt} \Psi =\psi(x) \frac{df}{dt} \\
\frac{ \partial^{2}\Psi }{ \partial x^{2} } =f(t)\frac{d^{2}\psi}{dx} \\
\end{align}
$$
These two combine to give us
$$
\begin{align}
-\frac{\hbar}{2m}f(t)\frac{d^{2}\psi}{dx^{2}}+V(x)\psi(x)f(t)=i\hbar \psi(x) \frac{df}{dt}
\end{align}
$$
We can multiply the whole equation by $\frac{1}{f(t)\psi(x)}$ to separate the equation.

$$
\begin{align}
-\frac{\hbar^{2}}{2m} \frac{1}{\psi(x)} \frac{d ^{2}\psi}{dx^{2}} +V(x)=i\hbar \frac{1}{f(t)} \frac{d f}{dt} =E 
\end{align}
$$
These must be conserved since one side only varies with time and another only with space, and varying one won't change the other. We set both of these sides to equal E, a constant, and make two equations:
$$
\begin{align}
\frac{i\hbar}{f(t)} \frac{d f}{dt} =E \\
\frac{d f}{dt} =-\frac{i}{i}E f(t)\to  f(t)=f(0)e^{\frac{-iEt}{\hbar}}\\
\end{align}
$$
(side note, $\frac{1}{i}=-i$)

We can absorb $f(0)$ into $\psi(x)$, and set a variable $w=\frac{E}{\hbar}$. This gives us the spinning function of time dependence $e^{-i\omega t}$.
$$
\begin{align}
\Psi(x,t)=\psi(x)e^{-i\omega t}
\end{align}
$$
We can find the probability amplitude
$$
\begin{align}
\left| \Psi(x,t) \right|^{2} = \left| \psi(x) \right|^{2} 
\end{align}
$$
(since we take the complex conjugate which removes the $e^{-i\omega t}$ portion). 

## Particle in a box

We have an energy function that is kind of fake, but indulge:
$$
\begin{align}
V(x)=\begin{cases}
0 & 0\leq x\leq L \\
\infty & \text{ else }
\end{cases}
\end{align}
$$
Note that the wave function must be continuous, since we have to be able to take two derivatives.
$$
\begin{align}
\Psi(x)=\begin{cases}
 \text{ to find } & x < l\\ 
0 & x\geq L, x\leq 0
\end{cases}
\end{align}
$$

We take the original big equation:
$$
\begin{align}
-\frac{\hbar^{2}}{2m} \frac{1}{\psi(x)} \frac{d ^{2}\psi}{dx^{2}} +V(x)=i\hbar \frac{1}{f(t)} \frac{d f}{dt} =E 
\end{align}
$$
$E= -\frac{\hbar^{2}}{2m}\frac{1}{\psi}\frac{d ^{2}\psi}{dx^{2}}$
We can rewrite for $\frac{d ^{2}\psi}{dx^{2}}=-\frac{2mE}{\hbar}\psi=-k^{2}\psi$
Where $k=\sqrt{ \frac{2mE}{\hbar^{2}} }$

We want to make a wave function solution, so we set
$$
\begin{align}
\psi(x)=A\cos(kx)+B\sin(kx)
\end{align}
$$
To find the coefficients $A\text{ and } B$, we use what we know about the boundary: $\psi(0)=0,\psi(l)=0$
$\psi(0)=0\implies A=0$
$\psi(L)=0\implies B\sin kL=0$
$kL=n\pi,n \in \mathbb{N}$

This gives us
$$
\begin{align}
\Psi(x)=\begin{cases}
B\sin\left( \frac{n\pi}{L}x \right) & x < l,n \in \mathbb{N}\\ 
0 & x\geq L, x\leq 0
\end{cases}
\end{align}
$$
We can learn about B by normalizing so that this has a physical meaning.

We can write 
$$
\begin{align}
\Psi(x,y)=e^{-i\omega t}\psi(x) = \begin{cases}
B\sin\left( \frac{n\pi}{L}x \right)e^{-iEt/\hbar},\text{ in the box, }n=1,2 \\
0 \text{ outside the box }
\end{cases}
\end{align}
$$
We have defined $k=\sqrt{ \frac{2mE}{\hbar} }$, and have just put the restriction with the sin that $k=\frac{n\pi}{L}$. This means... energy must be quantized!!
$E_{n}=\frac{\pi^{2}\hbar^{2}n^{2}}{2mL^{2}},n \in\mathbb{N}$

Anyways, let's go back to finding out about B.

$$
\begin{align}
\int_{-\infty}^{\infty} \left| \Psi(x,t) \right| ^{2}dx=1 \\
\int_{0}^{L} \lvert B^{2} \rvert \sin ^{2}\left( \frac{n\pi}{L}x \right)dx \\
\text{ we can use the trig relation } \\
\sin ^{2}\theta=\frac{1}{2}(1-\cos(2\theta))
\end{align}
$$
This gives us
$$
\begin{align}
\lvert B \rvert ^{2}\int_{0}^{L} \frac{1}{2}\left( 1-\cos\left( \frac{2n\pi}{L}x \right) \right)dx  \\
1=\lvert B \rvert ^{2} \left[ \frac{L}{2}-\frac{L}{2n\pi}\underbrace{ \sin\left( \frac{2n\pi}{L}x \right) }_{ 0 } \bigg|_{0}^{L}   \right]  \\
\lvert B \rvert ^{2}=\frac{2}{L} \\
B=\sqrt{ \frac{2}{L} }e^{-\delta}, \text{ we choose } \delta=0
\end{align}
$$
