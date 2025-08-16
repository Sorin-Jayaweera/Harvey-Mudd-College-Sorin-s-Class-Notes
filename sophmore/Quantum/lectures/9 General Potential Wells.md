![[Pasted image 20250210100705.png|300]]

But if we raise the energy
![[Pasted image 20250210100734.png|300]]

## General potential wells
![[Pasted image 20250210101049.png|300]]
Lets write out the time independent Schrödinger equation
$$
\begin{align}
-\frac{\hbar^{2}}{2m} \frac{ \partial^{2} }{ \partial x^{2} } \psi+v(x)\psi=E\psi \\
\frac{ \partial^{2} }{ \partial x^{2} } \psi=-\frac{2m}{\hbar^{2}}(E-v(x))\psi
\end{align}
$$
We note that 
$$
\begin{align}
\frac{ \partial^{2} }{ \partial x^{2} } \psi=0 \text{ when } E=v(x), \text{ i.e. at a,b } \\
\text{ also, } \frac{ \partial^{2} }{ \partial x^{2} } \psi=0 \text{ when } \psi=0 \text{ (node) }
\end{align}
$$

If we have $E>V_{x}$
$$
\begin{align}
\frac{ \partial^{2} }{ \partial x^{2} } \psi=-k^{2}(x)\psi, ~ k(x)\equiv \frac{\sqrt{ 2m(E-v(x)) }}{\hbar}
\end{align}
$$
This gives us the curvature $\propto$ $-\text{ function }$. So everywhere, it will curve towards the x-axis.

The $k(x)$ equation tells us that 
$$
\begin{align}
\lambda(x)=\frac{2\pi}{k(x)}=\frac{2\pi \hbar}{\sqrt{ 2m(E-v(x)) }}
\end{align}
$$
When $E-V(x)$ is bigger, we have a smaller wavelength and a smaller amplitude.
When $E$ is close to $V(x)$, we have a large wavelength and large amplitude.

![[Pasted image 20250210101943.png|400]]

We can also look when $E<V(x)$
$$
\begin{align}
\frac{ \partial^{2} }{ \partial x^{2} } \psi = \frac{2m}{\hbar^{2}}(V(x)-E)\psi \\
\frac{ \partial^{2} }{ \partial x^{2} } \psi\equiv \kappa^{2}(x)\psi \implies \text{ decaying solutions } \\
\kappa(x)\equiv \frac{\sqrt{ 2m(V(x)-E) }}{\hbar}
\end{align}
$$
We have a decay length 
$$
\begin{align}
\frac{1}{\kappa (x)}  & = \frac{1}{\sqrt{ 2m(V(x)-E) }} \\
\text{ Bigger } V(x)-E \to   & \text{ Smaller decay length} \\
 & \text{ aka faster decay speed  }
\end{align}
$$
$$
\begin{align}
e^{-kx}\approx e^{\frac{-x}{'l'}}, \text{ 'l' = decay length }
\end{align}
$$
So curvature $\propto$ function.

Hold up... don't we need the wave function to go to zero at infinity?

![[Pasted image 20250210102432.png|400]]

We can't find a bound state anywhere that the energy is above the potential function. The function, following the proportionality, would look like this:
![[Pasted image 20250210102921.png|300]]
This is not normalizable. 

Lets consider a funky stepping energy function.
Where we have a long distance, we have a short wavelength. When the energy is closer, we have longer wavelengths. This requires the steepness to be more for the short wavelengths, and less for the long one.

![[Pasted image 20250210103608.png|300]]
We therefore see that the particle is more likely to be found in a location where the kinetic energy is smaller. 


Any bound state will end up with quantized energies. 

## Bound states of general potential wells
$$
\begin{align}
\frac{ \partial^{2} }{ \partial x^{2} } \psi= -\frac{2m(E-V(x))}{\hbar}\psi \\
\frac{ \partial^{2}\psi }{ \partial x^{2} }=0 \text{ when } E=V(x) \text{ or } \psi=0 \\
\psi_{n} \text{ has } n-1 \text{ nodes } 
\end{align}
$$
![[Pasted image 20250210104419.png|300]]

We have
$$
\begin{align}
\psi_{Ⅰ}=A_{1}\sin(k_{1}x+\phi_{1}) \\
\psi_{Ⅱ}=A_{2}\sin(k_{2}x+\phi_{2})
\end{align}
$$
$$
\begin{align}
k_{n}=\frac{\sqrt{ 2m(E-V_{n}) }}{\hbar} \\
k_{1} > k_{2}
\end{align}
$$
We have to enforce
$$
\begin{align}
\psi_{Ⅰ}(0)=\psi_{Ⅱ}(0) \\
 & \left[ A_{1}\sin(\phi_{1})=A_{2}\sin(\phi_{2}) \right] ^{2} \\
\frac{ \partial \psi_{Ⅰ} }{ \partial x } \bigg|_{x=0}^{} =\frac{ \partial \psi_{Ⅱ} }{ \partial x }   \bigg|_{x=0}^{}   \\
 & \left[ A_{1}\cos \phi_{1}=\frac{k_{2}}{k_{1}}A_{2}\cos(\phi_{2}) \right]^{2}
\end{align}
$$
This gets us the system of equations
$$
\begin{align}
A_{1}^{2}=A_{2}^{2}\left[ \sin ^{2}(\psi_{2}) + \left( \frac{k_{2}}{k_{1}} \right)^{2}\cos ^{2}(\phi_{2})-\cos ^{2}\phi_{2}\right]  \\
A_{1}^{2}=A_{2}^{2} \left\{ 1+ \left[ \left( \frac{k_{2}}{k_{1}} \right)^{2}-1 \right] \cos ^{2}(\phi_{2}) \right\} 
\end{align}
$$
This implies $A_{2}>A_{1}$.

This tells us that when we are in the wiggly regions, the smaller the wavelength the smaller the amplitude. 


