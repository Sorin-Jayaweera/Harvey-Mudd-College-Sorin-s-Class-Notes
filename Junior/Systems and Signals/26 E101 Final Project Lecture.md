
Design, build, and test a low pass filter to produce a $10$ Hz sinusoidal signal from a $10$ Hz pulse train. 

We will make an analog and digital filter.

We will make a pulse train generator, then build a circuit for analog filtering, and then use the modified comb filter from homework 9b to filter in an Arduino.

![[Pasted image 20251202102445.png]]

We will build a 2 stage sallen key circuit.

![[Pasted image 20251202102534.png]]
![[Pasted image 20251202102545.png]]

The pulse train has a fundamental frequency, but also higher harmonics. We are trying to get rid of those harmonics so that we can get a pure sinusoidal signal from the fundamental frequency.

Then we will use a digital filter.

Comb filter:
$$
\begin{align}
H(z) = b(1-z^{-m}) \\
\end{align}
$$
And the modified comb filter to actually use
$$
\begin{align}
H(z) = \Pi_{k=2} ^{M-2} b_{0} (1-e^{-jk \frac{2\pi}{M}}z^{-1})
\end{align}
$$

This is designed to eliminate harmonics at those harmonic frequencies. 

We should get something close to a pure sine. 
