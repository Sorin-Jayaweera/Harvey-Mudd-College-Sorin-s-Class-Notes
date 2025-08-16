
![[Pasted image 20250305130603.png]]

We have the Fourier transform defined as 
$$
\begin{align}
\tilde{f}= \int_{-\infty}^{\infty} e^{-i\omega t}f(t)dt \\
f(t)=\frac{1}{2\pi}\int_{-\infty}^{\infty} e^{i\omega t}\tilde{f}(\omega)d\omega
\end{align}
$$
and that 
$$
\begin{align}
\frac{1}{2\pi}\int_{-\infty}^{\infty} e^{i\omega t}d\omega=\delta(t)
\end{align}
$$
## A
If $f(t)$ is real, then we can  evaluate both $\tilde{f}(-\omega) \text{ and } \tilde{f}(\omega)^{*}$
$$
\begin{align}
\tilde{f}(-\omega)= \int_{-\infty}^{\infty} e^{i\omega t}f(t)dt \\
\tilde{f}(\omega)^{*} = \int_{-\infty}^{\infty} e^{-i\omega t^{*}} f(t)dt \\ = \int_{-\infty}^{\infty} e^{i\omega t}f(t)dt \\
\end{align}
$$
We can see that these expressions are equivalent, so $\tilde{f}(-\omega)=\tilde{f}(\omega)^{*}$.
## B) 
the Fourier series of $f$ will have the same parity as $f$.
We can show this by taking even and odd functions
The Fourier is defined as:
$$
\begin{align}
\int_{-\infty}^{\infty} e^{-i\omega t}f(t) dt
\end{align}
$$
For an even function $f(x),$ we have the property $f(x)=f(-x)$
For an odd function $g(x),$ we have the property $g(x)=-g(-x)$

We just have to show that 
$$
\begin{align}
\int_{-\infty}^{\infty} e^{-i\omega t}dt
\end{align}
$$
is even. If it is, then it will respect the parity of any function multiplied to it.

We can take the Fourier of an even function (so that we won't change the parity of the Fourier operator) and see if it is even:
$$
\begin{align}
\int_{-\infty}^{\infty} e^{-i\omega t}f(t)dt \stackrel{?}{=}  \int_{\infty}^{-\infty} e^{i\omega t}\underbrace{ f(-t) }_{ f(t) }d(-t) \\
\end{align}
$$
From here we can simplify the right side
$$
\begin{align}
\int_{-\infty}^{\infty} - e^{i\omega t}f(-t)d(-t) \\
\int_{-\infty}^{\infty}  e^{i\omega t}f(-t)d(t) \\
\tilde{f}(\omega)=\int_{-\infty}^{\infty}  e^{i\omega t}f(t)dt
\end{align}
$$
We can check $\tilde{f}(-\omega)$
$$
\begin{align}
\int_{-\infty}^{\infty} e^{-i(-\omega) t}f(t)dt \\
\int_{-\infty}^{\infty} e^{i\omega t}f(t)dt \\

\end{align}
$$
We see that these two are the same, so the Fourier series of an even function will be even.

If instead the function were odd, we can do the same
$$
\begin{align}
\int_{-\infty}^{\infty} e^{-i\omega t}f(t)dt \stackrel{?}{=}  \int_{\infty}^{-\infty} e^{i\omega t}\underbrace{ f(-t) }_{ -f(t) }d(-t) \\
\end{align}
$$

$$
\begin{align}
\int_{-\infty}^{\infty} - e^{i\omega t}f(-t)d(-t) \\
\int_{-\infty}^{\infty}  e^{i\omega t}f(-t)d(t) \\
\tilde{f}(\omega)=\int_{-\infty}^{\infty}  -e^{i\omega t}f(t)dt
\end{align}
$$
We can check this against $\tilde{f}(-\omega)$
$$
\begin{align}
\int_{-\infty}^{\infty} e^{-i(-\omega) t}f(t)dt \\
\int_{-\infty}^{\infty} e^{i\omega t}f(t)dt \\
\end{align}
$$
We can see that
$$
\begin{align}
\tilde{f}(\omega)=-\tilde{f}(-\omega)
\end{align}
$$
so if the function $f(t)$ is odd, then the Fourier transform will be odd, and if the $f(t)$ is even that the Fourier will be even.

## C
If $f(t)$ is imaginary and odd, then I would expect the Fourier series to be real and odd.

## D)
![[Pasted image 20250310135658.png]]
We can show that this is commutative by checking if
$f*g\stackrel{?}{=} g*f$

$$
\begin{align}
\int_{-\infty}^{\infty} g(t')f(t-t')dt' \stackrel{?}{=}  \int_{-\infty}^{\infty} f(t-t')g(t')dt' \\

\end{align}
$$
Because multiplication is commutative, we can rearrange the right side to be

$$
\begin{align}
\int_{-\infty}^{\infty} g(t')f(t-t')dt' \stackrel{?}{=} \int_{-\infty}^{\infty} g(t')f(t-t')dt'
\end{align}
$$
which is true.

![[Pasted image 20250305130619.png]]
$$
\begin{align}
\tilde{f}= \int_{-\infty}^{\infty} e^{-i\omega t}f(t)dt \\
f(t)=\frac{1}{2\pi}\int_{-\infty}^{\infty} e^{i\omega t}\tilde{f}(\omega)d\omega
\end{align}
$$
A) I would expect this to be real and even, since the function is real and even. 

B)
Our function is spatial, not temporal, so we need to use spatial frequencies.
$$
\begin{align}
\tilde{f}(k)= \int_{-a}^{a} e^{-ikx}A(a-\left| x \right| )dx \\
= A\int_{-a}^{a}  ae^{-ik x}-\left| x \right| e^{-ik x}dx \\
\end{align}
$$
We can split this into the left and right sides for inside the integral:
$$
\begin{align}
\text{ left: } \\
= \left[ \frac{a}{ik}e^{-ik x} \right]\bigg|_{-a}^{a} \\
= -\frac{a}{ik } (e^{ika}-e^{-ika})   \\
= -2i \frac{a}{ik}\sin(ka) \\
= -2 \frac{a}{k}\sin(ka)
\end{align}
$$

We can do the right side with two separate integration by parts:

$$
\begin{align}
\int_{-a}^{a} \left| x \right| e^{-ikx}dx = \int_{-a}^{0} -xe^{-ikx}dx +\int_{0}^{a}   xe^{-ikx}dx \\
= -\left[ \frac{xe^{-ikx}}{-ik}+\frac{e^{-ikx}}{k^{2}} \right]\bigg|_{-a}^{0} + \left[ \frac{xe^{-ikx}}{-ik}+\frac{e^{-ikx}}{k^{2}} \right] \bigg|_{0}^{a}  \\
= - \left[ \frac{1}{k^{2}}-\frac{ae^{ika}}{ik} -\frac{e^{ika}}{k^{2}}\right]  + \left[ \frac{ae^{-ika}}{-ik}+\frac{e^{-ika}}{k^{2}}-\frac{1}{k^{2}} \right] \\
= -\frac{2}{k^{2}} +\frac{ae^{ika}}{ik}-\frac{ae^{-ika}}{ik}+\frac{e^{ika}}{k^{2}}+\frac{e^{-ika}}{k^{2}} \\
=-\frac{2}{k^{2}} + \frac{a}{ik}(2i\sin(ka))+ \frac{1}{k^{2}}(2\cos(ka)) \\
=-\frac{2}{k^{2}}+\frac{2\cos(ka)}{k^{2}}+\frac{2a\sin(ka)}{k} \\
=\frac{2(\cos(ka)-1)}{k^{2}}+\frac{2a\sin(ka)}{k}
\end{align}
$$



Therefore we get
$$
\begin{align}
A\left[  - \frac{2a}{k}\sin(ka)-\frac{2(\cos(ka)-1)}{k^{2}}+\frac{2a\sin(ka)}{k} \right] \\
\end{align}
$$
$$
\begin{align}
\tilde{f}(k)= \frac{2A(1-\cos(ka))}{k^{2}} 
\end{align}
$$

## c)
This looks like a gaussian distribution almost, where we have a lot of low frequency waves and very few high frequency, since our function looks fairly linear and should not be fluctuating a lot. Because the function is real and even, we would expect the Fourier to be real and even. 

###### Side note: I thought that the Fourier of a real function would be imaginary, but this isn't?


 
![[Pasted image 20250305130653.png]]

$$
\begin{align}
\tilde{f}= \int_{-\infty}^{\infty} e^{-i\omega t}f(t)dt \\
\end{align}
$$
$$
\begin{align}
\tilde{f}= A \int_{-\infty}^{\infty} xe^{-\alpha x^{2}-i\omega x} dx \\
\end{align}
$$
We can set
$$
\begin{align}
e^{-\alpha x^{2}-i\omega x}  = u
\end{align}
$$
$$
\begin{align}
\frac{ d u}{d w } = -ixe^{-\alpha x^{2}-i\omega x} \\
\end{align}
$$

We can rewrite our integral with this:

$$
\begin{align}
A \int_{-\infty}^{\infty} xe^{\alpha x( i\omega-x) } dx \\
= A \int_{-\infty}^{\infty} -\frac{1}{i} \frac{ d }{d w } u\,  dx  \\
= Ai \frac{ d }{d \omega }  \int_{-\infty}^{\infty} u dx \\
\end{align}
$$
We can solve this integral:
$$
\begin{align}
\int_{-\infty}^{\infty} e^{-\alpha x^{2}-i\omega x}dx \\
\end{align}
$$
This is an identity that we have, it simplifies to
$$
\begin{align}
\sqrt[]{ \frac{\pi}{\alpha} } e^{(i\omega)^{2}/(4 \alpha)}\\
=\sqrt[]{ \frac{\pi}{\alpha} } e^{-\omega^{2}/(4 \alpha)}
\end{align}
$$

Therefore, we get our Fourier series as
$$
\begin{align}
A \sqrt[]{ \frac{\pi}{\alpha} } \frac{ d }{d \omega }
e^{\frac{-\omega^{2}}{4 \alpha}} \\
= A \sqrt[]{ \frac{\pi}{\alpha} } \left( -\frac{2\omega}{4\alpha} \right)e^{\frac{-\omega^{2}}{4\alpha}} \\
\tilde{f} = -\frac{A\omega}{2} \sqrt[]{ \frac{\pi}{\alpha^{3}} } e^\frac{-\omega^{2}}{4\alpha}
\end{align}
$$

![[Pasted image 20250305130706.png]]
We can find this:
$$
\begin{align}
\tilde{f}= \int_{-\infty}^{\infty} e^{-ikx}Ae^{-a\left| x \right| }dx \\
= \int_{-\infty}^{\infty} Ae^{-ikx}e^{-a\left| x \right| }dx \\
\end{align}
$$
We can break up the bounds:
$$
\begin{align}
A \left[ \int_{-\infty}^{0} e^{-ikx}e^{-a(-x)} dx + \int_{0}^{\infty} e^{-ikx}e^{-ax}dx\right]  \\
= A \left[ \int_{-\infty}^{0} e^{x(a-ik)}dx + \int_{0}^{\infty} e^{-x(ik+a)} dx\right]  \\
= A \left[ \frac{e^{x(a-ik)}}{a-ik}\bigg|_{-\infty}^{0}- \frac{e^{-x(ik+a)}}{ik+a}\bigg|_{0}^{\infty}\right]   
\end{align}
$$

$$
\begin{align}
= A \left[ \frac{1}{a-ik} - \frac{1}{a+ik} \right]  \\
= A \left[ \frac{a+ik - a+ik}{a^{2}+k^{2}} \right]  \\
= \frac{2Aik}{a^{2}+k^{2}} 
\end{align}
$$



