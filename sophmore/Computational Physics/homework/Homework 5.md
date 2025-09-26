![[Pasted image 20250219184843.png]]

We can write out our function as
$$
\begin{align}
f(t) = a_{0}+\sum_{n=1}^{\infty} a_{n}\sin\left( \frac{n\pi t}{\tau} \right)+b_{n}\cos\left( \frac{n\pi t}{\tau} \right)
\end{align}
$$

I will find the average first
$$
\begin{align}
\int_{0}^{\tau} f(t)dt = \int_{0}^{\frac{\tau}{2}}\sin(\omega t)dt \\
\frac{1}{\omega}(\cos(\omega t))\bigg|_{0}^{\frac{\tau}{2}} \\
a_{0} = \frac{1}{\tau} \frac{2}{\omega} \\
a_{0} = \frac{1}{\pi}  
\end{align}
$$


We can also solve for our coefficients $a_{n}$ and $b_{n}$.
$$
\begin{align}
\int_{0}^{\frac{\tau}{2}} \sin(\omega t)\sin(n\omega t)dt = \int_{0}^{\tau} a_{n}\sin ^{2}(n\omega t)dt
\end{align}
$$
We can solve this right side as
$$
\begin{align}
\frac{a_{n}}{2}\int_{0}^{\tau} (1-\cos(2n\omega t))dt \\
= \frac{a_{n}}{2}\left( 1-\frac{1}{2n\omega}\sin(2n\omega t) \right) \bigg|_{0}^{\tau} \\
= \frac{a_{n}}{2}  
\end{align}
$$
We can do the left side with the trig identity
$$
\begin{align}
\sin a\sin b = \frac{1}{2 }\left[ \cos(a-b)-\cos(a+b) \right] 
\end{align}
$$
This yields
$$
\begin{align}
\frac{1}{2}\int_{0}^{\frac{\tau}{2}}  \cos(\omega t-n\omega t)-\cos(\omega t+n\omega t)dt \\
\frac{1}{2}\int_{0}^{\frac{\tau}{2}}  \cos((1-n)\omega t)-\cos((1+n)\omega t)dt \\
= \frac{1}{2}\left[\frac{1}{(1-n)\omega t} \sin((1-n)\omega t) -\frac{1}{(1+n)\omega t} \sin((1+n)\omega t) \right] \bigg|_{0}^{\frac{\tau}{2}}   \\
\end{align}
$$
$$
\begin{align}
=\frac{1}{2} \left[ \frac{1}{(1-n)\pi}\sin((1-n)\pi) - \frac{1}{(1+n)\pi}\sin((1+n)\pi)\right] 
\end{align}
$$
We know that $\frac{\sin(x)}{x} \implies 1 \text{ as }x \implies 0$. Elsewhere, this function is zero.
At $n=1$, this gets $\frac{1}{2}$
At $n=-1$, we get $-\frac{1}{2}$
$n$ is only positive, so we have 
$$
\begin{align}
a_{n} =\begin{cases}
\frac{1}{2}, & n=1 \\
0  & \text{ else }
\end{cases}
\end{align}
$$

We can also do the cosine components,
$$
\begin{align}
\int_{0}^{\frac{\tau}{2}} \sin(\omega t)\cos(n\omega t)dt = \int_{0}^{\tau} b_{n}\cos ^{2}(n\omega t)dt \\
\end{align}
$$
I will do the left side first. We have the identity
$$
\begin{align}
\sin a\cos b = \frac{\sin(a+b)+\sin(a-b)}{2}
\end{align}
$$
We can simplify down to

$$
\begin{align}
\int_{0}^{\frac{\tau}{2}} \frac{\sin(\omega t+n\omega t)+\sin(nt-n\omega t)}{2}dt \\
= \frac{1}{2}\int_{0}^{\frac{\tau}{2}} \sin((1+n)\omega t) + \sin((1-n)\omega t)dt \\
= \frac{1}{2} \left[ \frac{1}{(1+n)\omega}\cos((1+n)\omega t)+\frac{1}{(1-n)\omega}\cos((1-n)\omega t) \right] \bigg|_{0}^{\tau/2}   \\
= \frac{1}{2  }\left[  \frac{1}{(1+n)\omega}\cos((1+n)\pi)+\frac{1}{(1-n)\omega}\cos((1-n)\pi) - \frac{1}{(1+n)\omega}-\frac{1}{(1-n)\omega}\right]
\end{align}
$$

The cos will follow
$$
\begin{align}
\begin{bmatrix}
n  & 0 & 1 & 2 & 3 \\
\cos((1+n)\pi)  & -1 & 1 & -1 & 1 \\
\cos((1-n)\pi) & -1 &  1 & -1 & 1
\end{bmatrix}
\end{align}
$$
So this expression collapses to
$$
\begin{align}
\frac{1}{2} \left[ (-1)^{n+1}  \left( \frac{1}{(1+n)\omega} + \frac{1}{(1-n)\omega}\right) - \frac{1}{\omega}\left( \frac{1}{1+n}+\frac{1}{1-n} \right)  \right] 
\end{align}
$$


$$
\begin{align}
= \frac{1}{2 } \left[ \frac{1}{\omega}  \frac{1-n+1+n}{1-n^{2}}\left( (-1)^{n+1}-1 \right)  \right]  \\
=\frac{1}{\omega} \frac{1}{1-n^{2}} \left[ (-1)^{n+1}-1 \right] 
\end{align}
$$
We can solve the right side to get
$$
\begin{align}
b_{n}\int_{0}^{\tau} \cos ^{2}(n\omega t)dt \\
= \frac{b_{n}}{2} \int_{0}^{\tau} 1+\cos(2n\omega t)dt  \\
= \frac{b_{n}}{2} \left[ \tau+\sin(4\pi n) \right] \\
= \frac{b_{n}\tau}{2} 
\end{align}
$$
Therefore, we get
$$
\begin{align}
\frac{b_{n}\tau}{2} = \frac{1}{\omega} \frac{1}{1-n^{2}} \left[ (-1)^{n+1}-1 \right] \\

b_{n} = \frac{1}{\pi} \frac{1}{1-n^{2}} \left[ (-1)^{n+1}-1 \right]
\end{align}
$$
Therefore, we get the series as
$$
\begin{align}
f(t)  = \frac{1}{\pi} + \frac{1}{2}\sin(\omega t) + \sum_{n=1}^{\infty}   \frac{1}{\pi} \frac{1}{1-n^{2}} \left[ (-1)^{n+1}-1 \right] \cos(n\omega t)
\end{align}
$$


![[Pasted image 20250219184851.png]]
Yes, all the terms scale by $\frac{1}{n^{2}}$.

![[Pasted image 20250219184901.png]]

This is surprisingly good!
![[Pasted image 20250223164137.png]]

