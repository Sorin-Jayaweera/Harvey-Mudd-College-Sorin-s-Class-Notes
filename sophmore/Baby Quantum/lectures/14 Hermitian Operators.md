We have a new operator: Parity. We define 
$\Pi_{op}f(x)=f(-x)$
This is reflecting the function about the $y$ axis.

We have
$$
\begin{align}
\Pi_{op}  f_{\lambda}(x) = \lambda f_{\lambda}(x)
\end{align}
$$
$$
\begin{align}
\Pi_{op}  \Pi_{op}  f_{\lambda}(x)= \Pi_{op}  (\lambda f_{\lambda}(x))=\lambda^{2}f_{\lambda}(x) = f_{\lambda}(x)
\end{align}
$$
We know that this has to be true, so $\lambda^{2}=1$.
If $f_{\lambda}$ is an even function, $\lambda=1$
If $f_{\lambda}$ is odd, then $\lambda=-1$.

$\Pi_{op}$ eigenvalues are real.
$\Pi_{op}$ eigenfunctions are orthogonal:
$$
\begin{align}
\int_{-\infty}^{\infty} f_{\text{ even }}^{*}f_{\text{ odd }}dx=0
\end{align}
$$

For example:
Energy eigenstates for potential energies that are centered at $x=0$ alternate between even and odd eigenfunctions. 

Consider an infinite square well of width $a$, centered at $x=0$.
What is the probability of an odd parity measurement if we act on a state with wave function given by:
$$
\begin{align}
\psi(x)=\frac{1}{2}\psi_{1}+\frac{\sqrt{ 3 }}{2}\psi_{2}(x)  \\
\end{align}
$$
We can draw out the two eigenfunctions:
![[Pasted image 20250221102004.png|300]]
$P(\text{ odd })= \left| \frac{\sqrt{ 3 }}{2} \right|^{2}=\frac{3}{4}$

Lets explore:
$$
\begin{align}
f(x)=\frac{f(x)}{2}+\frac{f(x)}{2} + \frac{f(-x)}{2}-\frac{f(-x)}{2} \\
f(x) = \frac{1}{2}\left[\underbrace{  f(x)+f(-x)  }_{ \text{ even } }\right] + \frac{1}{2}\left[ \underbrace{ f(x)-f(-x) }_{ \text{ odd } } \right] 
\end{align}
$$

This left side is even, since if we swap x to -x it keeps the value.
The right side is odd, since since it becomes the opposite.

This is the statement that for any function $f(x)$, we can write it as a sum of eigenstates of the parity operator with eigenvalues $+1\text{ and } -1$.

The Hamiltonian operator also has real eigenvalues, has a complete set of energy eigenfunctions, and is normalizible. We see these properties for other operators.

## Introducing Hermitian operators. 

$A_{op}$ is Hermitian if 
$$
\begin{align}
\int_{-\infty}^{\infty} (A_{op}  \Phi)^{*}\Psi dx = \int_{-\infty}^{\infty} \Phi ^{*}A_{op}  \Psi dx
\end{align}
$$
for any complex wavefunctions $\Psi,\Phi$.
$$
\begin{align}
\Leftrightarrow  \left< A \right>  = \int_{-\infty}^{\infty} \Psi^{*} A_{op}  \Psi dx \text{ is Real }
\end{align}
$$
For any Hermitian operator 
$$
\begin{align}
\text{ real eigenvalues }A_{op}  \psi _{n}=a_{n}\psi _{n}, \,  a_{n} \in  \mathbb{R} \\
\text{ orthogonal eigenfunctions }: \int_{-\infty}^{\infty} \psi^{*}_{m}\psi _{n}dx = 0 \, \text{ if  }m \neq n \\
\text{ we form a complete set of eigenfunctions }: \\
\psi(x,0) = \sum_{n}^{\infty}  c_{n} \psi _{n},  \\
c_{n}(0) = \int_{-\infty}^{\infty} \psi _{n}^{*}\Psi(x,0) dx \\
\end{align}
$$


Is $p_{x,op}$ Hermitian?
$$
\begin{align}
\left< P_{x} \right>  ^{*}= \left< p_{x} \right>  ? \\
\left< p_{x} \right>  ^{*} = \left[ \int_{-\infty}^{\infty} \Psi^{*}  \frac{\hbar}{i} \frac{d}{dx} \Psi dx \right]^{*} \\
= \int_{-\infty}^{\infty} \frac{\Psi \hbar}{-i} \frac{d}{dx} \Psi^{*}  dx = -\frac{\hbar}{i}\int_{-\infty}^{\infty} \Psi d\Psi^{*} \\   
\end{align}
$$
We can get this into a nicer form with integration by parts.
$$
\begin{align}
-\frac{\hbar}{i} \left[\underbrace{  \Psi\Psi^{*}   \bigg|_{-\infty}^{\infty} }_{ 0, \stackrel{\text{ bc normalizable }}{\text{ so 0 at  }\pm \text{ inf }}  } - \int_{-\infty}^{\infty} \Psi^{*} d\Psi \right]
\end{align}
$$
Which goes to
$$
\begin{align}
\frac{\hbar}{i}\int_{-\infty}^{\infty} \psi^{*} \frac{d\psi}{dx} = \int_{-\infty}^{\infty} \Psi^{*} \frac{\hbar}{i} \frac{d }{dx} \Psi dx = \left< P_{x} \right>   
 \end{align}
$$

We claim that 
$$
\begin{align}  
\text{ for } A_{op}  \psi _{n} n=a_{n}\psi _{n}, \, \, \, 
a_{n}=a_{n}^{*}
\end{align}
$$
We choose $\Phi=\Psi=\psi _{n}$
$$
\begin{align}
\int_{-\infty}^{\infty} (A_{op}  \Psi _{n} )^{*} \psi _{n}dx = \int_{-\infty}^{\infty} \psi _{n}^{*}A_{op}\psi _{n} dx
\end{align}
$$
We can act the operator on each term to get
$$
\begin{align}
\int_{-\infty}^{\infty} a_{n}^{*}\psi _{n}^{*}\psi _{n}dx = \int_{-\infty}^{\infty} a_{n}\psi _{n}^{*}\psi _{n}dx
\end{align}
$$
Which gives us
$$
\begin{align}
a_{n}=a_{n}^{*}, \text{ so the eigenvalues are real. }
\end{align}
$$
What about the orthogonality thing?

## Orthogonality
Lets choose different eigenstates.
$\Phi=\psi _{n}, \Psi=\psi_{m}$
We can write
$$
\begin{align}
\int_{-\infty}^{\infty} (A_{op}  \psi _{n}^{*}) \psi _{n} dx = \int_{-\infty}^{\infty} \psi _{n}^{*}A_{op}  \psi _{n} dx \\
a_{n}^{*}\int_{-\infty}^{\infty} \psi _{n}^{*}\psi _{n}dx=a_{n}\int_{-\infty}^{\infty} \psi _{n}^{*}\psi _{n}dx
\end{align}
$$
This becomes
$$
\begin{align}
(a_{n}-\underbrace{ a_{m} }_{ a_{m}=a_{m}^{*} }) \int_{-\infty}^{\infty} \psi _{n}^{*}\psi _{n}dx = 0
\end{align}
$$
If $a_{n}\neq a_{m}$




