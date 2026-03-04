These are a great consequence of bosons being social!

Light amplification by Stimulated Emission of Radiation.


## Light-Atom interactions
Imagine an electron at an energy level. A photon with frequency $\nu$ corresponding to the energy difference from the current energy level to the next could be absorbed by the electron - Absorption. Similarly, the electron could fall an energy level and release the same type of photon. That's Emission.

Lets say we have $N_{2}$ atoms with electrons in energy $E_{2}$, and $N_{1}$ with energy $E_{1}$.

$$
\begin{align}
\frac{ d N_{2}}{d t } = -\frac{ d N_{1}}{d t } 
\end{align}
$$
We define
$B_{12}\rho(T,\nu)$ as the probability of absorption per unit atom ($T=$ temperature). This depends on some constant and the number density of photons at that frequency.

We also define $A_{21}$ is the probability of emission per atom per time. 
$$
\begin{align}
\frac{ d N_{2}}{d t } = B_{12} \rho(T,\nu)N_{1}
\end{align}
$$

At thermal equilibrium,
$$
\begin{align}
\frac{n_{2}}{n_{1}}=e^{\frac{-(E_{2}-E_{1})}{k_{B}T}}
\end{align}
$$
The bigger the energy difference, the fewer in state $E2$ relative to $E_{1}$. 
We would also expect $\frac{ d n_{2}}{d t }=0$. 

This would give us
$$
\begin{align}
B_{12} \rho(T,\nu)N_{1}=A_{21} N_{2}
\end{align}
$$
Try to solve for $\rho(T,\nu)$. This is $\frac{A_{21}}{B_{12}}e^{\frac{-h\nu}{k_{B}T}}$.
## Stimulated Emission
This looks almost like spontaneous emission. If we pass a single photon by an electron in state $E_{2}$, then it will fall and emit another photon. There is a statistical weighting factor that is increased when there is a photon nearby. The system is extra "happy" to put a photon in the same state that it is in. This is identical boson magic. 

We can write out:
$$
\begin{align}
\frac{ d N_{2}}{d t } = B_{12}\rho(T,\nu)N_{1} - A_{21} N_{2} - B_{21} \rho(T,\nu)N_{2}
\end{align}
$$
In equilibrium, this means
$$
\begin{align}
\rho(T,\nu) = \frac{A_{21}}{B_{12} \frac{N_{1}}{N_{2}} - B_{21} } \\
= \frac{A_{21}}{B_{12} (e^{\frac{h\nu}{k_{B}T}}-B_{21} )}
\end{align}
$$
We have
$$
\begin{align}
\rho_{bb} (T,\nu) = \frac{8\pi h\nu^{3}}{c^{3}(e^{(\frac{h\nu}{k_{B}T})}-1)}
\end{align}
$$
We can now solve for the coefficients relative to each other. 

## Einstein A and B coefficients
$$
\begin{align}
A_{21}  = \left( \frac{8\pi h\nu^{3}}{c^{3}} \right)B \\
B_{21} =B_{12} =B
\end{align}
$$


![[Pasted image 20250409103903.png]]

## Gain

$$
\begin{align}
\text{ Rate of emission  } = N_{2}A_{21} (1+n_{be} (E,T))
\end{align}
$$

The rate of emission of photons is related to the number of bosons, which depends on the rate of photons. Uh oh!

Lets draw a box with volume $V$ and incoming photons.
$$
\begin{align}
\frac{ d N_{2}}{d t } = B \rho(T,\nu)(N_{1}-N_{2}) \\
\frac{ d }{d t } \rho(T,\nu)\Delta v= -\frac{ d }{d t } \frac{N_{2}h\nu}{V}
\end{align}
$$
We can plug these together to get
$$
\begin{align}
\frac{ d \rho(T,\nu)}{d t } = B \frac{h_{2}}{V\Delta t}(N_{2}-N_{1})\rho(T,\nu)
\end{align}
$$
For photons, $\frac{ d x}{d t }=c$. This gives
$$
\begin{align}
\frac{ d \rho(T,\nu)}{d x } = B \frac{h\nu}{V\Delta \nu c}(N_{2}-N_{1})\rho(T,\nu)
\end{align}
$$
We have a derivative of a thing in terms of the thing and constants... time for $e$! 
$$
\begin{align}
\rho(t,\nu)= \rho(\nu,0 )e^{\alpha x} \\
\alpha= B \frac{h\nu}{V\Delta vc}(N_{2}-N_{1})
\end{align}
$$
where $\alpha$ is the gain constant. 

We have a box with photons coming in, and as the wave travels it depletes the number that are in $N_{2}$, but keep moving forward to a new area that hasn't been depleted yet. We have an exponentially increasing number of photons as you go every tiny bit. 

How does energy conservation work? 
in a normal system, we have more things in the lower state than the upper state