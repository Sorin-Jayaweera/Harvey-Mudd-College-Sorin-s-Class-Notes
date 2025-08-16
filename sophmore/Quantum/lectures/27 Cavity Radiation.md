
For bosons or fermions at any temperature,

$$
\begin{align}
N \equiv  \int_{0}^{\infty} n(E)D(E)dE \\
E_{tot} = \int_{0}^{E_{f}} E D(E)dE  
\end{align}
$$
## Blackbody radiation

If matter and EM radiation are in thermal equilibrium with each other, the spectrum of radiation that an object will emit depends on the temperature, not composition of the material or shape. We'll generalize later to see how it works for stars or things that aren't in equilibrium.


### EM Radiation in a hollow conducting box
Take a box with side lengths $l$ that is hollow, with metal walls (conductors).
![[Pasted image 20250402101607.png|300]]

We have

$$
\begin{align}
\nabla^{2}\vec{\mathcal{E}} = \frac{1}{c^{2}} \frac{ \partial^{2} }{ \partial t^{2} } \underbrace{ \vec{\mathcal{E} } }_{ \text{ electric field } } \\
\vec{\mathcal{E} } = \vec{\mathcal{E} }_{x}\hat{i}+\vec{\mathcal{E} }_{y}\hat{j}+\vec{\mathcal{E} }_{z}\hat{k}   \\
\nabla^{2}\vec{\mathcal{E} }_{x} = \frac{1}{c^{2}} \frac{ \partial^{2} }{ \partial t^{2} } \mathcal{E} _{x} \\
\text{ etc } 
\end{align}
$$
We can use separation of variables 
$$
\begin{align}
\mathcal{E} _{x} = X(x)Y(y)Z(z)f(t)
\end{align}
$$


#### Constraints on $\vec{\mathcal{E}}$
We know that the electric field will be perpendicular to the surface of the metal, since it is a conductor. 
$$
\begin{align}
\mathcal{E} _{\mid\mid }=0 \text{ on conductor } 
\end{align}
$$
Inside the box, we don't have any contained charges, so
$$
\begin{align}
\vec{\nabla}\cdot  \vec{\mathcal{E} } = 0
\end{align}
$$

#### Solution
$$
\begin{align}
\mathcal{E}_{x} = \mathcal{E}_{x}  \cos\left( \frac{n_{x} \pi x}{l} \right)\sin\left( \frac{n_{y}\pi y}{l}  \right) \sin\left( n_{z} \frac{\pi z}{l} \right)\sin(\omega t) \\
\text{ etc for } \mathcal{E_{y} },\mathcal{E_{z} } \text{ but with cos on the relevant parameter }  
\end{align}
$$

On the back wall of the box, we are allowed to have an x component, and have zero for the others. 


#### Dispersion:
We take the unknown parameters $\omega$ and $n$, and plug into our differential equation
$$
\begin{align}
\nabla^{2}\mathcal{E_{x} } = \frac{1}{c^{2}}\frac{ \partial^{2} }{ \partial t^{2} } \mathcal{E_{x}} 
\end{align}
$$
To get the dispersion relation
$$
\begin{align}
\left( \frac{\pi}{L} \right)^{2}(n_{x}^{2} +n_{y}^{2}+n_{z}^{2}  ) = \frac{1}{c^{2}}\omega^{2}
\end{align}
$$
$$
\begin{align}
E=\hbar \omega = \hbar \frac{c\pi}{L}(n_{x} ^{2}+n_{y} ^{2}+n_{z} ^{2})^{\frac{1}{2}=}\hbar \frac{c\pi}{L}\underbrace{ r }_{ \text{ radius in n-space } }
\end{align}
$$

## Density of states for photons

Consider,
$$
\begin{align}
E_{tot} = \sum_{i}^{} n_{be} (E_{i} )E_{i} \\
\text{ (all quantum states) } \\
\approx \int_{0}^{\infty} \underbrace{ D(E) }_{ \text{ density of states per energy } }\underbrace{ n_{be} }_{ \text{ n bose einstein } }\underbrace{ E }_{ energy }   dE
\end{align}
$$

We consider all quantum states, adding the total volume closed in an octant (which will give us the number of states modulo the spin degeneracy factor).

![[Pasted image 20250402102455.png|300]]
$$
\begin{align}
V_{\text{ shell }} = \frac{1}{8} 4 \pi r^{2} dr
\end{align}
$$
Each cube corresponds to one position space state. We have the total number of states, where each cube has lengths 1, and multiply by the number of states per cube (spin degeneracy factor). 

For a photons (spin 1), we have two states. $l=1,m_{l}=\pm 1 \text{ (no 0) }$
So the total number of states is
$$
\begin{align}
\text{ \# states } = 2 \frac{1}{8} 4\pi r^{2} dr
\end{align}
$$
We have energies that are a function of $R$:
$$
\begin{align}
E =  \frac{\hbar c \pi}{L}r, \implies r = \frac{L}{\hbar c\pi}E, \\
dr = \frac{L}{\hbar c\pi}dE
\end{align}
$$
We don't have to change the bounds of our integral because both go from $0\text{ to }\infty$. 
$$
\begin{align}
E{tot } = \int_{0}^{\infty} \frac{\pi L^{2}}{\hbar^{2}c^{2}\pi^{2}}E^{2} \frac{L}{\hbar c\pi }dE \, n_{\text{be}} E \\
E_{tot} = \int_{0}^{\infty}\underbrace{  \frac{L^{3}E^{2}}{\hbar^{3}c^{3}\pi^{2}} }_{ D(E) }n_{\text{be}} (E)E dE
\end{align}
$$
Lets reiterate because it is generally useful:
$\boxed{D(E)= \frac{L^{3}E^{2}}{\hbar^{3}c^{3}\pi^{2}}}$

We've done the first of 4 changes of variables. Lets go from energy to frequency.
$$
\begin{align}
E=h\nu
\end{align}
$$
$$
\begin{align}
E_{tot} = \int_{0}^{\infty} \frac{L^{3}\nu^{2}8 \pi}{c^{3}}\, n_{\text{be}} \, h\nu \, \, d\nu  
\end{align}
$$

Recall that 
$$
\begin{align}
n_{be} (E) = \frac{1}{e^{\frac{E-\mu}{k_{B}T}}-1}
\end{align}
$$
Which can be rewritten as
$$
\begin{align}
n_{be} (h\nu) = \frac{1}{e^{\frac{h\nu}{k_{B}T}}-1} 
\end{align}
$$
Therefore, our total energy can be written as

$$
\boxed{
\begin{align}
E_{tot} = \int_{0}^{\infty} \frac{8\pi L^{3}h}{c^{3}} \frac{\nu^{3}}{e^{\frac{h\nu}{k_{B}T}}-1} d\nu
\end{align}
}
$$
The energy density inside the cavity depends only on the temperature. 

## Plank Function
$$
\begin{align}
\frac{E_{tot}}{L^{3}} = \int_{0}^{\infty} \rho(\nu)d\nu \\
\rho(\nu)= \frac{8\pi h\nu^{3}}{(e^{\frac{h\nu}{k_{B}T}}-1)c^{3}}  &  & \frac{\text{ Energy Density }}{\text{ frequency }}  
\end{align}
$$

This gives us a "spectrum". Hotter is bluer, higher frequency is blue. 

![[Pasted image 20250402103958.png|300]]


We can very similarly write this out for wavelength,
![[Pasted image 20250402104041.png|300]]


## Wein's Law
We can think about how the peak wavelength changes as a function of temperature. 

Consider:
$$
\begin{align}
\frac{d\rho(\lambda)}{d \lambda}=0 \implies \lambda_{\text{ max }} =  \frac{2.9\times 10^{-3}m\cdot K}{T} 
\end{align}
$$

We have the color of an object given by this. As $T$ increases, $\lambda_{\text{ max }}$ decreases.

The sun is $T_{\text{ sun }}=5800k$, so $\lambda_{sun} = \frac{2.9\times 10^{-3}}{5800} \approx 500 nm$. This is greenish blue.

For a person, this is $\frac{2.9\times 10^{-3} m}{300K}= 10 \mu m, \text{ infrared }$. 

## Total Energy Density Inside the Cavity

![[Pasted image 20250402104858.png]]

This is Stephan Boltzmann's temperature relation.

We quantized the allowed modes of radiation for photons, solved for the amount of energy in a box, and found a temperature relation for the energy in a box. 