## Harmonic Series
We have the harmonic series:
$$
\begin{align}
H=\sum_{n=1}^{\infty} \frac{1}{n}=1+\frac{1}{2}+\frac{1}{3}+\dots
\end{align}
$$
This does not converge. How do we prove that?
We can make a curve that is always below the sum, $\frac{1}{x}$, and try to integrate. This integral does not converge, so the sum can't have a finite value.

We can do the opposite, taking an integral that is always above the series and showing that it converges, allowing the sum to converge.

Lets take something else:
$$
\begin{align}
s=\sum_{n}^{\infty} a_{nj}; \sum_{n=0}^{\infty} a_{0}r^{n} \\
\text{ converges for } \left| r \right| <1
\end{align}
$$
How do we 
know what this would go down to?
$$
\begin{align}
s_{n}= & a_{0}(1+ & r+r^{2}+\dots+ & r^{n}) \\
r s_{n} =  & a_{0}( & r +r^{2}+\dots+ & r^{n}+r^{n+1})
\end{align}
$$

We can subtract these two. This gets us
$$
\begin{align}
s_{n}(1-r)=a_{0}(1-r^{N+1}) \\
s_{n}=a_{0} \frac{1-r^{N+1}}{1-r}
\end{align}
$$

We can do something nifty with r. 
$r=\left| r \right|e^{i\phi}$
$\left| r \right|^{n+1}=e^{i(n+1)\phi}$.

Lets look at the old homework problem:
$$
\begin{align}
\bar{E}=\frac{\sum_{n=0}^{\infty} e^{-\beta \hbar \omega \left( \frac{n+1}{2} \right)}\hbar \omega \left( n+\frac{1}{2} \right)}{Z}
\end{align}
$$
We can recognize that this could be simplified with
$$
\begin{align}
\frac{-\frac{ \partial  }{ \partial \beta } \sum_{n=0}^{\infty} e^{-\beta \hbar \omega \left( \frac{n+1}{2} \right)}}{Z} \\
\text{  we now have a geometric series, with r =  } e^{-\beta \hbar \omega}   \\
\bar{E}= \frac{-\frac{ \partial  }{ \partial \beta } Z}{Z}= -\frac{ \partial  }{ \partial \beta } ln(Z)\\
\text{ also note that  } Z \equiv \sum_{n=0}^{\infty} e^{-\beta \hbar \omega \left( \frac{n+1}{2} \right)} \\
\text{ so }  \\
Z=e^{-\beta \hbar \omega \frac{1}{2}} \sum_{n=0}^{\infty} r^{n} \text{ where } r = e^{-\beta \hbar \omega}
\end{align}
$$

Now, we can simplify this to
$$
\begin{align}
Z= e^{-\beta \hbar \omega \frac{1}{2}} \frac{1}{1-e^{-\beta \hbar \omega}} \\
\text{ multiply top and bottom } \\
Z = \frac{1}{e^{\beta \hbar \omega/2}-e^{-\beta \hbar \omega/2}} \\
z = \frac{1}{2\sinh\left( \beta \hbar \frac{\omega 1}{2} \right)}
\end{align}
$$


We can look at some fun series:
$$
\begin{align}
S=1-\frac{1}{2}+\frac{1}{3} - \frac{1}{4} +\frac{1}{5} - \dots
\end{align}
$$
We can group terms in this to be either
$1-\frac{1}{6}-\frac{1}{20}\dots$
or
$$
\begin{align}
\frac{1}{2}+\frac{1}{12}+\frac{1}{30}\dots
\end{align}
$$
So this must be bounded between $\frac{1}{2} \text{ and } 1$

However,
$$
\begin{align}
\frac{1}{2}-\frac{2}{3}+\frac{3}{4}-\frac{4}{5}\dots
\end{align}
$$
goes to $+1-1+1-1\dots$ which doesn't converge.

## Taylor Series

![[Pasted image 20250206102455.png]]
We can use these for others in nifty ways:
$$
\begin{align}
sech (x) = \frac{1}{\cosh x} \\
\text{ sechx } = \frac{1}{1+\underbrace{ \frac{x^{2}}{2!}+\frac{x^{4}}{4!}+\dots }_{ q }} \\
\text{ we can use the expansion of  } \frac{1}{1+x} \text{ to get } \\
1-q+q^{2}-q^{3}\dots
\end{align}
$$
We can find which values of q will generate a certain power, and compute an approximation up to that power.

## Gamma Function
$\Gamma(n+1)=\int_{0}^{\infty}x^{n}e^{-x}dx$



