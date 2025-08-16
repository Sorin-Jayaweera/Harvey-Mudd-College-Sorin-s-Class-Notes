
How do we evaluate $n!$ for large $n$?
$$
\begin{align}
1\times  2\times  3\times  \dots\times n
\end{align}
$$This is valuable in statistical mechanics, since we have to count number of microstates which uses $n\choose k$ for huge numbers.

What if instead we wrote $ln(n!)=ln_{1}+ln(2)+ln(2)$
We could make a plot displaying this:
![[Pasted image 20250211095424.png|300]]

We can bound this value by integrating
$$
\begin{align}
ln(N!)  & < \int_{1}^{n+1} ln(x)dx \\
 & =xlnx\bigg|_{1}^{N+1}-\int_{1}^{N+1} x \frac{1}{x}dx \\
ln(n!)  & < (N+1)ln(N+1)-N \\
\end{align}
$$
We can also bound the bottom side by shifting the ln(x-1), so that it moves right 1 unit. 

We write
$$
\begin{align}
ln(n!) & > \int_{2}^{n+1} ln(x-1)dx  \\
 & = N ln(N) - N+1
\end{align}
$$
This gets a decent bound. If we put in
$$
\begin{align}
6! = 720 \\
ln(6!)=6.579 \\
7ln(7)-6=7.621 \\
6ln(6) = 5.75
\end{align}
$$
We can do this better with the gamma function.

We can write
$$
\begin{align}
\Gamma(n+1) & =\int_{0}^{\infty} \underbrace{ x^{n} }_{ u } \underbrace{ e^{-x}dx }_{ dv } \\
 & = \underbrace{ -x^{n}e^{-x}\bigg|_{0}^{\infty} }_{ 0 } +\int_{0}^{\infty} nx^{n-1}e^{-x}dx 
\end{align}
$$
We see that this latter part is the same thing that we had before, so we have the recurrence relation:
$$
\begin{align}
\Gamma(n+1) & =n\Gamma(n) \\
 & =n(n-1)(n-2)\dots\underbrace{ (2) }_{ n=1 }\underbrace{ (1) }_{ n=1 }
\end{align}
$$
This looks like the factorial. However, the gamma function is fine if $n$ is a complex number, real, fractional, anything.

The fact that we have an integral in the function means we can use a series to describe it.

![[Pasted image 20250211100659.png|300]]
This is a very sharp function, but we can smoothen it out by applying $ln$, so that we can later Taylor expand and keep the results useful for a decent range.
$$
\begin{align}
y=ln(x^{n}e^{-x})=nlnx-x \\
y'=\frac{n}{x}-1 \implies y'=0 \text{ at } x=n
\end{align}
$$
Most of the area is going to be located near the maximum at $x-n$.

We can use this y to find $n!$, $$
\begin{align}
\int_{0}^{\infty} e^{y}dx \approx n!
\end{align}
$$


Let's do a Taylor expansion for $y$ around the maximum:

$$
\begin{align}
y(x)\approx y(n)+ y'(n)x + \frac{y''x^{2}}{2} +\dots
\end{align}
$$
$$
\begin{align}
y'=\frac{n}{x}-1 \\
y''=-\frac{n}{x^{2}} \\
y''' = \frac{2n}{x^{3}} \\
 \\
y'(n)=0 \\
y''(n)=-\frac{1}{n} \\
y'''(n)=\frac{2}{n^{2}}
\end{align}
$$

So this gives us the Taylor series around the peak
$$
\begin{align}
y\approx \underbrace{ nln(n)-n }_{ y(n) } + \underbrace{ \frac{1}{2!}\left( -\frac{1}{n} \right)(x-n)^{2} }_{ y''(n) } + \underbrace{ \frac{1}{3!}\frac{2!}{n^{2}}(x-n)^{3} }_{ y'''(n) }
\end{align}
$$

We can see the pattern here:
$$
\begin{align}
y^{iv}(n)=-\frac{3!}{n^{3}}\dots \text{ we get the whole series }
\end{align}
$$
We can write this as a sum.

Let $\xi=x-n$
$$
\begin{align}
n! \approx \int_{-n}^{\infty} e^{nln(n)-n - \frac{\xi^{2}}{2n}+\frac{\xi^{3}}{3n^{2}}-\frac{\xi^{4}}{4n^{3}}+\dots} d\xi\\
\end{align}
$$
Note that we set the lower bound to $-n$ since we change variables to $\xi$.

Okay, now were gonna get a bit hairy.
Lets ignore $\xi^{3}$ and higher.
$$
\begin{align}
n! \approx \int_{-n}^{\infty} e^\frac{nln(n)-n-\xi^{2}}{2n}d\xi \\
= n^{n}e^{-n}\int_{-n}^{\infty} e^{\frac{-\xi^{2}}{2n}} & d \xi
\end{align}
$$
This... isn't among the class of integrals that we know how to do. But! What if we take $n\to \infty$? Then we do know this.

Take the identity that 
$$
\begin{align}
\int_{-\infty}^{\infty} e^{-\alpha x^{2}}dx=\sqrt{ \frac{\pi}{\alpha} }
\end{align}
$$
How bad of an error would we be making if we take the limit as $n\to  \infty$? 
![[Pasted image 20250211102642.png|400]]

With our approximation, we get
$$
\begin{align}
n! & =n^{n}e^{-n}\sqrt{ \frac{\pi}{\frac{1}{2n}} } \\
 & = \sqrt{ 2\pi n }n^{n}e^{-n}
\end{align}
$$
We can compare this number with the actual $n!$, and see that it gets close a lot faster than our original expression of $\frac{n^{n}e^{-n}}{n!}$. 
This is called Sterling's expansion for the curious.

Lets analyze this more. 
$$
\begin{align}
q\equiv \frac{\xi^{3}}{3n}-\frac{\xi^{r}}{4n^{3}}+\frac{\xi^{5}}{5n^{4}}-\frac{\xi^{6}}{6n^{5}}-\frac{\xi^{6}}{6n^{5}} \\
\alpha\equiv \frac{1}{2n}
\end{align}
$$
$$
\begin{align}
n! = n^{n}e^{-n}\int_{-\infty}^{\infty} e^{-\alpha \xi^{2}}e^{q}d\xi
\end{align}
$$

As $\xi$ gets big (compared to n), this series will blow up!  (or will it?)
We can be delicate here. Lets represent $e^{q}$ as $1+q+\frac{q^{2}}{2!}+\dots$ 
When we do it this way, then we see that $e^{-\alpha \xi^{2}}$ always wins. 

We see, when we are trying to evaluate this, the terms that were going to have in the polynomial will all be in $q$, aka polynomials in $\xi$ multiplying $e^{-\alpha \xi^{2}}$. We can ask a smaller question to help us. Lets define:
$$
\begin{align}
I_{m}\equiv \int_{-\infty}^{\infty} \xi^{m}e^{-\alpha \xi^{2}}d\xi
\end{align}
$$
Half of those are easy. If $m$ is odd, the integral is $0$ (the odd function from $-\infty$ to $\infty$ will cancel out to zero). We only have to worry about the even ones!
Lets integrate by parts, and find only the even terms of $m$.
$$
\begin{align}
I_{2m}=\int_{-\infty}^{\infty} \xi^{2m}e^{-\alpha \xi^{2}} d\xi \\
=\int_{-\infty}^{\infty} \left( -\frac{ \partial  }{ \partial \alpha }  \right)^{m} e^{-\alpha \xi^{2}}d\xi \\
\end{align}
$$
We can yank this out, and get
$$
\begin{align}
I_{2m}=\left( -\frac{ \partial  }{ \partial \alpha }  \right) ^{m}\sqrt{ \frac{\pi}{\alpha} }
\end{align}
$$
