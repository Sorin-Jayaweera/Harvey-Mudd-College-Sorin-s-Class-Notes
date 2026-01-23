
 If something is highly percussive / exists for a small amount of time, it will have energy across all frequencies. All pass filters allow all frequencies, but your recording might have phase delay behavior - smearing out the sound. If a signal has been distorted in a way, all pass filters (have a 1 at all frequencies) can be used to correct the phase distortion. 

For instance, 
$$
\begin{align}
Y(s) = \frac{1}{s} - \frac{1}{s+1}, \mathrm{Re}\left\{ s \right\} > 0 \\
y(t) = u(t) - e^{-t}u(t)
\end{align}
$$
This is on the edge of being stable - it approaches $1$ as $\mathrm{Re}\left\{ s \right\}\to \infty$, not $0\text{ or }\infty$. 
$$
\begin{align}
\left| H(j\omega) \right| = 1
\end{align}
$$

Unilateral vs Bilateral:
$$
\begin{align}
\int_{-\infty}^{\infty} x(t)e^{-st}dt \\
\int_{0}^{\infty} x(t)e^{-st}dt
\end{align}
$$




## Review from E79

Lets say we have a causal LTI given by
$$
\begin{align}
y''(t) + 3y'(t) + 2y(t) = x(t)
\end{align}
$$
with initial conditions
$y(0^{-})=2, y'(0^{-})=0$.
(note that $0^{-}$ means just instantaneously before time $t=0$).

We take the $\mathscr{L}\text{aplace transform }$
$$
\begin{align}
s^{2}Y(s) - sy(0^{-}) - y'(0^{-}) + 3[sY(s)-y(0^{-})] + 2Y(s)  = X(s) \\
Y(s)[s^{2}+3s+=2]  = \frac{1}{s} + 2s + 6  \\
Y(s) = \frac{2s^{2}+6s+1}{s(s+2)(s+1)} = \frac{A}{s} + \frac{B}{s+2} + \frac{C}{s+1} \\
y(t) = (A+Be^{-2t}+ Ce^{-t})u(t)
\end{align}
$$

### Laplace summary

* What is Laplace? $X(s)= \int_{-\infty}^{\infty}x(t)e^{-st}dt$
* Take the Laplace usually with tables and properties, but can manually calculate. 
* Inverse laplace with the same thing, noting partial fraction decomposition.
* Interpreting Laplace: 
	* Region of convergence, Right or left sided
	* $X(j\omega)=X(s) \bigg|_{s=j\omega}^{}$
* When to Laplace: When passing an $X(s)$ through $H(s)$ to get $Y(s).

### Application: Filter Design
![[Pasted image 20251118101753.png]]
Lets say we want to filter out high frequency noise from a sensor measurement. We want to have a passband where the signal is almost entirely kept ($1\pm\delta$), we want a stopband where the signal is attenuated --  guaranteed rejection of frequencies by some amount, and an intermediary stage (the transition region).

In practice, when designing a filter we set some parameters for these.

At the passband, we want 
$$
\begin{align}
\left| H(j_{0}) \right| = 1 \\
\end{align}
$$
We want the 3dB point to have
$$
\begin{align}
\frac{\left| H(j\omega_{p} ) \right| }{H(j_{0})} = \frac{1}{\sqrt[]{ 2 } }
\end{align}
$$
And by the time we hit the stop band, we usually want -20 dB:
$$
\begin{align}
\frac{\left| H(j\omega_{s} ) \right| }{\left| H(j_{0}) \right| } = \frac{1}{10}
\end{align}
$$


Questions to ask:
How well does it pass the desired frequencies: $\delta_{1}, \omega_{p}$
How well does it block unwanted frequencies: $\delta_{2}, \omega_{s}$
How sharp is the transition: $\frac{\omega_{s}}{\omega_{p}}$

We build the filter by picking the pole and zero locations, then build a circuit / system that has that behavior.

Lets look at examples.

Butterworth filters are extremely useful given their sharp transition. The order of the filter tells you how many poles we have.

For instance, a second order butterworth:
$$
\begin{align}
H(s) = \frac{\omega_{c} ^{2}}{(s-\omega_{c}e^{j \frac{3\pi}{4}} )(s-\omega_{c} e^{-j \frac{3\pi}{4}})}
\end{align}
$$
This has poles symmetric across the $x$ axis at $\frac{3\pi}{4} \text{ and } -\frac{3\pi}{4}$.

That simplifies to
$$
\begin{align}
\left| H(j\omega) \right| = \frac{1}{\sqrt[]{ 1+ \left( \frac{\omega}{\omega_{c} } \right)^{4} } }
\end{align}
$$
We can build this now.
$$
\begin{align}
\frac{\left| H(j\omega_{p} ) \right| }{\left| H(j0) \right| } = \frac{1}{\sqrt[]{ 2 } } = \frac{1}{\sqrt[]{ 1+ \left( \frac{\omega_{p}}{\omega_{c} }  \right)^{4} } }
\end{align}
$$
Which tells us $\omega_{c}=\omega_{p}$. 

How far we put the poles from the origin (the radius) tells us the cutoff frequency.

Lets find the stopband:
$$
\begin{align}
\frac{\left| H(j\omega_{s} ) \right| }{\left| H(j0) \right| } = \frac{1}{\sqrt[]{ 1+ \left( \frac{\omega_{s}}{\omega_{c} }  \right)^{4} } } = \frac{1}{10}
\end{align}
$$
This tells us that
$$
\begin{align}
1+ \left( \frac{\omega s}{\omega_{c} } \right)^{4}  & = 100 \\
\omega_{s} ^{4}  & = 99 \omega_{c} ^{4} \\
\omega_{s}  & = \sqrt[4]{ 99 } \omega_{c} \\
\omega_{s}  & \approx 3.15 \omega_{p}  
\end{align}
$$
We pick the cutoff frequency, which determines the stopband frequency at roughly $3x$ the cutoff. The transition is fairly big - but we can make higher order Butterworth filters (4th, 6th, 9th) that cutoff way faster. 

We make these filters in circuit:
Lets look at the Sallen-key OpAmp circuit
![[Pasted image 20251118101845.png]]

We can use Kirchhoff's voltage and current laws with ideal op amps:
$$
\begin{align}
\frac{V_{out}(s)}{V_{in}(s) } = \frac{1}{s^{2}c_{1}c_{2}R_{1}R_{2}+s(R_{1}+R_{2})C_{2}+1}
\end{align}
$$
Using the relations we derived before for the cutoff frequency, we get:
$$
\begin{align}
c_{1}c_{2}R_{1}R_{2} = \frac{1}{\omega_{c}^{2} } \\
(R_{1}+R_{2})C_{2} = \frac{\sqrt[]{ 2 }}{\omega_{c} } 
\end{align}
$$

$$
\begin{align}
\text{ Butterworth }H(s) &  = \frac{\omega_{c} ^{2}}{s^{2}+\sqrt[]{ 2 } \omega_{c}s + \omega_{c}^{2}  }\\
 & =\frac{1}{\frac{1}{\omega_{c}^{2} }s^{2} + \frac{\sqrt[]{ 2 }}{\omega_{c} }s + 1 }
\end{align}
$$


