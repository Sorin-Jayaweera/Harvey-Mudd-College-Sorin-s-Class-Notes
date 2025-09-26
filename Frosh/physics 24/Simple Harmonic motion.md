
Springs:
Imagine stretching a spring, we have $F_{spr}=-kx$. What is the speed / acceleration as a function of position?
$$
\begin{align}
F_{net,x} = m \ddot{x}\\
-kx = m\ddot{x}\\
m\ddot{x}+kx=0 \\
\ddot{x}+\frac{k}{m}x=0 \\
\text{ let } \omega= \sqrt{ \frac{k}{m} } \\
\ddot{x}+\omega^{2}x=0 \\
\text{has the general solution} \\
x(t)=A\cos(\omega t+\phi_{0}).  \\
\text{ we can check that this is a valid solution: } \\
\dot{x}=-\omega A\sin(\omega t+\phi_{0}) \\
\ddot{x}=-\omega^{2} A\cos(\omega t+\phi_{0}) \\
\text{ Check the differential equation: } \\
-\omega^{2}A\cos(\omega t+\phi_{0})+\frac{k}{m}A\cos(\omega t+\phi_{0})\stackrel{?}{=} 0 \\
\text{ this works for  } \omega^{2}=\frac{k}{m}
\end{align}
$$

THEREFORE, if we see the second order differential equation
$$
\boxed{
\begin{align}
\ddot{x}+\omega^{2}x=0,\\
\text{ the solution is }\\
x(t) = A\cos(\omega t+\phi_{0})
\end{align}
}
$$
we have the requirement that $\omega T=2\pi$ where $T$ is the period.
$\omega=2\pi \nu$. $\phi_{0}$ is the initial phase of the oscillation
$\omega t+\phi_{0}$ is the phase at time $t$. 

$\omega$ is $\frac{2\pi}{\text{ time to do a full cycle }}$ so that $\omega t$ travels a full cycle in time $t$.  

## General simple harmonic oscillation
We use either $F_{net}=ma$ or $\frac{d}{dt}E=0$.
We then write the equation in the form
$$
\ddot{x}+\omega^{2}x=0
$$
We then get $\omega$ from the equation. 
$\omega=\frac{rad}{\text{ time }}=\text{ angular frequency}$.
$\nu=\frac{\text{ cycles }}{\text{ time }}, \nu=\frac{\omega}{2\pi}$. (hertz)
$T=\frac{\text{ time }}{\text{ cycle }}=\text{ period }=\frac{1}{\nu}=\frac{2\pi}{\omega}$. 

$\omega=\sqrt{ \frac{k}{m} }$ where $k$ is the restoring force, and $m$ is how much inertia the system has. 



