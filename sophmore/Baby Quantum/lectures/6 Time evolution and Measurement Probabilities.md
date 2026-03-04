![[Pasted image 20250203100914.png]]
We can advance each eigenfunction with time

$$
\begin{align}
\Psi(x,t) = \frac{1}{\sqrt{ 2 }}\Psi_{1}e^{\frac{-iE}{\hbar }t}
\end{align}
$$
We can now find the probability

$$
\begin{align}
\Psi(x,t)= \left( \frac{1}{\sqrt{ 2 }}\psi_{1}(x,t)e^{\frac{-iE}{\hbar}t} + \frac{1}{\sqrt{ 2 }}\psi_{2}(x,t)e^{\frac{-iE}{\hbar}t} \right) \left( \frac{1}{\sqrt{ 2 }}\psi_{1}(x,t)e^{\frac{iE}{\hbar}t} + \frac{1}{\sqrt{ 2 }}\psi_{2}(x,t)e^{\frac{iE}{\hbar}t} \right) 
\end{align}
$$
This gets
$$
\begin{align}
\frac{1}{2} \left( \Psi_{1}^{2}+\Psi_{2}^{2}+\Psi_{1}\Psi_{2}\left( e^{\frac{-i}{\hbar}(E_{2}-E_{1})t}+E^{\frac{i}{\hbar}(E_{2}-E_{1})t} \right) \right)  \\
= \underbrace{ \frac{1}{2} (\Psi_{1}^{2}+\Psi_{2}^{2}) }_{ \text{ constant background } } + \underbrace{ \Psi_{1}\Psi_{2}\cos\left( \frac{E_{2}-E_{1}}{\hbar}t \right) }_{ \text{ time dependence } }
\end{align}
$$
Our starting state was already a linearly independent sum of our two eigenstates. What if we have a really complicated function where we don't know how to break it up?

Well! We can decompose the function into an orthonormal basis set $\Psi_{n}$ to represent any $\Psi(x,0)$. 

$$
\begin{align}
\Psi(x,0)=\sum_{n}^{} \underbrace{ C_{n}(0) }_{ \text{ constants } }\underbrace{ \Psi_{n}(x) }_{ \text{ energy eigenstates } } \\
\text{ then } \\
\Psi(x,t) = \sum_{n}^{} c_{n}(0)\Psi_{n}(x)e^{-i \frac{E_{n}}{\hbar}t}
\end{align}
$$
And now we have any time dependent wave function! We just have to find these basis functions.

The result:
$$
\begin{align}
c_{n}(0)=\int_{-\infty}^{\infty} \Psi^{*} (x)\Psi(x,0) dx
\end{align}
$$

Lets derive this:
In $\mathbb{R}^{2}$ we can make an arbitrary vector in a coordinate space. 
![[Pasted image 20250203102831.png|300]]
We take a vector and take the dot product with each basis vector to find that component.

Lets go to a Hilbert Space!
![[Pasted image 20250203103035.png|300]]
For this space, we define the dot product of $\Psi_{n}$ with $\Psi(x,0)$ to be
$$
\begin{align}
c_{n}(0)=\int_{-\infty}^{\infty} \Psi_{n}^{*}(x)\Psi(x,0)dx
\end{align}
$$
This does the same thing as our dot product in $\mathbb{R}^{2}$. 

For example, lets take $c_{1}:$
$$
\begin{align}
c_{1}=\int_{-\infty}^{\infty} \Psi_{1}^{*}\left( \frac{1}{\sqrt{ 2 }}\psi_{1} + \frac{1}{\sqrt{ 2 }}\psi_{2} \right) dx \\
c_{1}=\int_{-\infty}^{\infty} \underbrace{ \frac{1}{\sqrt{ 2 }}\Psi_{1}^{*}\Psi_{1} }_{ \frac{1}{\sqrt{ 2 }}\text{ since } \left| \Psi_{1} \right| ^{2}=1 } + \underbrace{ \frac{1}{\sqrt{ 2 }}\Psi_{1}^{*}\Psi_{2}dx  }_{ \text{ 0 } }\\
\end{align}
$$
This falls from both physical intuition and the fact that they are orthonormal, so it fits with our definition of the dot product.

We have an orthonormality condition:
$$
\begin{align}
\int_{-\infty}^{\infty} \Psi_{m}^{*}\Psi_{n}dx=\begin{cases}
1 & \text{ if } m=n \\
0 & \text{ otherwies }
\end{cases}
\end{align}
$$
This is true for any possible energy eigen state for any bounding energy function. These eigenfunctions are sometimes called eigenvectors to make the comparison to linear algebra clear, since we could redo all of Quantum Mechanics with matrices. See the Big Quantum class (if I get to it). 


## Solving Initial Value Problems
1. Given: $V(x)$ and $\Psi(x,n)$ find $\Psi_{n}(x)$ by solving the time independent Schrödinger equation
2. Write that $\Psi(x,0)=\sum_{n}^{\infty}c_{n}(0)\Psi_{n}(x)$
3. $\Psi({x,t})$ is the same thing with the time dependence $\sum_{n}^{}c_{n}(0)e^{-i \frac{E_{n}}{\hbar}t}\psi_{n}$
4. To find $c_{n}(0): \Psi(x,0)=\sum_{n}^{}c_{n}(0)\psi _{n}(x)$
	We take the dot product with $\psi_{m}$. We do
	$\int_{-\infty}^{\infty}\psi_{m}^{*}\Psi(x,0)dx=\sum_{n}^{}\int_{-\infty}^{\infty}c_{n}(0)\psi _{n}\psi_{m}^{*}dx$
	$=\sum_{n}^{}c_{n}(0)\int_{-\infty}^{\infty}\underbrace{ \psi_{m}^{*}\psi_{n} }_{ \delta_{n,m} }dx$
	We have a special notation kroniker-delta $\delta_{n,m}$ that is 1 when $n=m$, 0 otherwise.
	$\int_{-\infty}^{\infty}\psi_{m}^{*}\psi(x,0)dx=c_{m}(0)$

fun note: if you measure the energy of a particle in some state that has coefficients $c_{m}(0)$, you will measure energy $E_{m}$ with probability $\left| c_{m} \right|$. 