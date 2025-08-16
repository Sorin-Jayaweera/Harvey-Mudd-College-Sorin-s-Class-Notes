#### Recall: 
The wave function relates time and spatial change of a wave, for which we have the solution $\Psi$. Using this equation for Psi below, we have baked in the energy momentum equation ($E=\hbar \omega,P=\hbar k$)

![[Pasted image 20250127100658.png]]

We normalize the wave function by setting 
$$
\begin{align}
\int_{-\infty}^{\infty} \Psi\Psi^{*} =1
\end{align}
$$
Normalization is required because we have a 100% probability of the electron/whatever being somewhere in space.

Because the equation is linear, we can add together multiple wave equations together and possibly normalize it to make another solution $\alpha \Psi_{1}+\beta \Psi_{2} \text{ where }\alpha \text{ and } \beta \text{ are complex }$

Then we could maybe have $\Psi(x,t) = \sum_{k}A_{k}e^{i(kx-\omega t)}$

>[!abstract]+ Definition: Wave Packets
>$\Psi(x,y) = \int_{-\infty}^{\infty}A(k)e^{i(kx-\omega t)}dk$
>This can be normalized, but we have to find the A(k) function. 

For example: Find $\Psi(x,0)$ for the following $A(k)$:
$$
\begin{align}
A(k)= \begin{cases}
A,k_{0}-\frac{\Delta k}{2} < k < k_{0}+ \frac{\Delta k}{2} \\
0,\text{ elsewhere }
\end{cases}
\end{align}
$$
$$
\begin{align}
\Psi(x,0) & =\int_{-\infty}^{\infty}A(k)e^{i(kx-\omega t)}dk \\
 & = \int_{k_{0}-\frac{\delta k}{2}}^{k_{0}+\frac{\delta k}{2}} Ae^{i(kx-\omega t)} dk\\
\text{ setting } t=0 \\
 & =A \frac{1}{ix} \left[ e^{ik\left( k_{0}+\frac{\Delta k }{2} \right)}-e^{ik\left( k_{0}-\frac{\Delta k}{2} \right)} \right] \\
 & =\frac{Ae^{ik_{0}x}}{ix}\left( e^{i\frac{\Delta k}{2}}-e^{-i\frac{\Delta k}{2}} \right)  \\
 & =\frac{Ae^{ik_{0}x}}{ix}2i\sin(\frac{\Delta k}{2}x) \\
 & =2Ae^{ik_{0}x}\sin(\frac{\Delta k}{2}x) \\
\end{align}
$$
We've seen this before. Let's take the complex square:
$$
\begin{align}
\Psi(x,0)^{2}=\frac{4A^{2}}{x^{2}}\sin ^{2}\left( \frac{\Delta k}{2}x \right) 
\end{align}
$$
We see that at $\frac{\Delta k x}{2}=\pi$ we find the first zeros (and at the sin argument =0, we have $\frac{0}{0}\implies 1$)

This tells us that $\Delta x\geq \frac{1}{2\Delta k}$
We can rewrite this as 
$$
\begin{align}
\Delta x\Delta k\geq  & \frac{1}{2},  \text{ which we can combine with }  p=\hbar k \text{ from physics } \\
\text{ to get the} & \text{  glorious hisenburg uncertainty principle: } \\
 & \Delta x\Delta p\geq \frac{\hbar}{2}
\end{align}
$$

We can also let our waves evolve over time. We have phase velocity and group velocity. 

Let's take a quick step back: with a single wavelength
$$
\begin{align}
\sin(kx-\omega t) & =\sin\left( k\left( x-\frac{\omega}{k}t \right) 
\right) \\
 & =\sin(k(x-vt)) \\
 & \text{ this is the phase velocity } V_{\text{ phase }}=\frac{\omega}{k}
\end{align}
$$
For two sines, we see that the wave speed is given by $V=\frac{\Delta w}{\Delta k}$. In the continuous limit, this becomes $V_{\text{ group }}=\frac{dw}{dk}$

For wave packets, the group velocity is the appropriate measure for how fast the wave is traveling. $V_{\text{ phase }}\neq V_{\text{ particle }}$.
$$
\begin{align}  & V_{\text{ phase }}=\\
 & \frac{w}{k}= \frac{\hbar w}{\hbar k}=\frac{\frac{p^{2}}{2m}}{p}=\frac{p}{2m} \\
 & =\frac{V_{\text{ particle }}}{2}
\end{align}
$$
However, 
$$
\begin{align}
V_{\text{ group }}= \\
\frac{d}{dk}(\omega)=\frac{d}{dk}\left( \frac{\hbar k^{2}}{2m} \right)=\frac{\hbar}{2m}(2k)=\frac{\hbar k}{m}=\frac{p}{m}=V_{\text{ particle }}
\end{align}
$$
The phase velocity is how fast each of the peaks is moving. The group velocity is how fast the wave packet looks like it is moving.

>[!abstract]+ Definition: Dispersion
>If the phase and group velocity are different from one another, then the overlap of the superimposed waves would change, so the wave packet would spread out and change


