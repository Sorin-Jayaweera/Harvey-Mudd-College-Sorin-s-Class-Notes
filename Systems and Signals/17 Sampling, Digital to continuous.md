Last time, we build a continuous to digital filter. Now we need to convert back, ideally an exact reconstruction of what we did before?


![[Pasted image 20251030103014.png]]

This works because we have the reconstruction filter, the thing that is a boxcar from $-\frac{\pi}{T}$ to $\frac{\pi}{T}$.
$$
\boxed{
\begin{align}
h(t)  & = \frac{1}{2\pi} \int_{-\infty}^{\infty} H(j\omega)e^{j\omega t}d\omega \\
 & = \frac{T}{2\pi} \int_{-\frac{\pi}{T}}^{\frac{\pi}{T}} e^{j\omega t}d\omega  \\
 & = \frac{T}{2\pi} \frac{1}{jt} e^{j\omega t} \bigg|_{-\frac{\pi}{T}}^{\frac{\pi}{T}}  \\
 & = \frac{T}{2\pi jt} \left( e^{\frac{jt \pi}{T}-}e^{-j \frac{t\pi}{T} } \right)  \\
 & = 2j \frac{\sin\left( \frac{\pi}{T}t \right)}{\frac{\pi t}{T}}
\end{align}
}
$$

The practical realistic solution, (because this goes from -inf to inf) is to have a zero order hold, where at each sample instant we hold it and make the next sample. This has an impulse response $h(t)$ that looks like a box of width T from 0 to T with height 1.
