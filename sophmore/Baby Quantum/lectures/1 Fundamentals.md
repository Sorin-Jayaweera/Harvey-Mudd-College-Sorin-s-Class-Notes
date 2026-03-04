>[!abstract]+ Definition: de Broglie Wavelength
>Every particle has an associated wavelength
>$\lambda_{db}=\frac{h}{p}, h=6.63\times 10^{-34}J\cdot s$
>For a non relativistic massive particle, we have:
>$\lambda_{dB}=\frac{h}{mv}$
>"Matter waves": even matter particles like electrons and atoms exhibit wave-like behavior

## Crystal diffraction:
In an experiment, electrons were shot on the surface of a nickel crystal. There are many paths that the electrons can travel and bounce off of. 
If the extra path length is an integer multiple of the wavelength, then the waves will be constructive. 
![[Pasted image 20250122100846.png]]

Can we find the separation between layers if we say that the maximum peak happened at theta = 65?

take that E=54ev.
$\lambda=\frac{h}{p}$
$k=\frac{p^{2}}{2m} \text{ take from  }k=\frac{1}{2}mv^{2}$
$2d\sin\theta=\lambda,$
$d=\frac{\frac{h}{\sqrt{ 2m_{e}*54ev }}}{2\sin(65)}$

## Photon Wave eq
Moving on, lets look at photon wave solutions.
Remember, $k=\frac{2\pi}{\lambda},\omega=\frac{2\pi}{T}$.

$$
\begin{align}
\frac{ \partial^{2}E_{z} }{ \partial x^{2} } =\frac{1}{c^{2}}\frac{ \partial^{2}Ez }{ \partial t^{2} } 
\end{align}
$$
We have two plane wave solutions,
$$
\begin{align}
\left\{ \sin(kx\pm \omega t),\cos(kx\pm \omega t) \right\} 
\end{align}
$$
$c=\frac{\lambda}{T}=\frac{\omega}{k}$
We have the dispersion relation for photons $\omega=ck$.

Lets guess the solution $A\cos(kx-\omega t)$
$$
\begin{align}
\frac{ \partial^{2} }{ \partial x^{2} } (A\cos(kx-\omega t))=-k^{2}A\cos(\dots) \\
\frac{ \partial^{2} }{ \partial t^{2} } ()=-\omega^{2}A\cos() \\
\text{ plug in: } -k^{2}A\cos() = \frac{1}{c^{2}}(-\omega^{2}A \cos()) \\
\implies k=\frac{\omega}{c}
\end{align}
$$

Lets take the energy momentum relationship:
$$
\begin{align}
E=h\nu = \hbar w \\
p = \frac{h}{\lambda}=\hbar k  \\ \\
\text{ and we know that } k=\frac{\omega}{c}
\frac{p}{\hbar}=\frac{\frac{E}{\hbar r}}{c} \\
\text{ therefore, we've derived }
E=pc
\end{align}
$$

## Matter Wave Equation: Reverse engineering the Schrodinger equation

Quantum energy & momentum relations of a free particle:
$$
\begin{align}
E=\frac{p^{2}}{2m}=\hbar \omega, P=\hbar k, \hbar\equiv \frac{h}{2\pi}
\end{align}
$$
This is the crazy idea that brings our classical picture of energy to momentum with the deBroglie momentum.
$\hbar \omega = \frac{\hbar^{2}k^{2}}{2m}$
$$
\boxed{
\begin{align}
\omega=\hbar \frac{k^{2}}{2m}
\end{align}
}
$$

The relativistic energy-momentum relation is encoded in the wave equation via its dispersion relation:
$$
\begin{align}
\frac{ \partial^{2}E_{z} }{ \partial x^{2} } =\frac{1}{c^{2}}\frac{ \partial^{2}E_{z} }{ \partial t^{2} } 
\end{align}
$$

This is the Schrödinger equation:
$$
\begin{align}
-\frac{\hbar^{2}}{2m}\frac{ \partial^{2} }{ \partial x^{2} }\Psi(x,t)+V(x)\Psi(x,y)=i\hbar \frac{ \partial  }{ \partial t }\Psi(x,t)
\end{align}
$$
We can break this down as kinetic energy + potential energy = total energy. We will later find that the kinetic energy expression is called the "Hamiltonian". 

For a free particle we have no forces, so we can simplify this down to 
$$
\begin{align}
-\hbar \frac{r^{2}}{2m}\frac{ \partial^{2} }{ \partial x^{2} } \Psi(x,t)=i\hbar \frac{ \partial  }{ \partial t } \Psi(x,t)
\end{align}
$$
Lets try guessing a solution. Let $\Psi(x,t)=A\cos(kx-\omega t)$.

$\frac{ \partial^{2} }{ \partial x^{2} }\Psi=-k^{2}\Psi$
$\frac{ \partial  }{ \partial t }\Psi \neq-\omega^{2}\Psi$
instead, $\frac{ \partial  }{ \partial t }\Psi=\omega A\sin(kx-\omega t)$. 
Therefore, this does not satisfy Schrödinger's equation. If we wanted to try this as a solution, we would take the first time derivative we would get

Lets try another guess: $\Psi(x,y)=Ae^{i(kx-\omega t)}$
$$
\begin{align}
\frac{ \partial^{2} }{ \partial x^{2} } \Psi=ik^{2}\Psi=-k^{2}\Psi \\
\frac{ \partial  }{ \partial t } \Psi=-i\omega \Psi
\end{align}
$$
This works as a solution for the photon wave equation, and we can try plugging it in to the Schrödinger equation. We get
$$
\begin{align}
-\frac{\hbar^{2}}{2m}(-k^{2}\Psi)=i\hbar (-i\omega \Psi) \\
\text{ we can rearrange this and compare the coefficients } \\
\frac{\hbar^{2}k^{2}}{2m}=\hbar \omega \\
w=\hbar \frac{k^{2}}{2m}
\end{align}
$$

Summary:
The Schrödinger equation encodes the correct energy-momentum relation for matter waves (reproduces de Broglie theory). For free matter waves: we must use complex exponentials! Solutions to the Schrödinger equation are irreducibly complex. This is the first fundamental equation in physics with an $i$ in it! But... physical observables must be real. So, what is $\Psi$.

We'll see next time, but $\Psi$ is an analog of $Z$ that we saw before, the complex probability amplitude.

