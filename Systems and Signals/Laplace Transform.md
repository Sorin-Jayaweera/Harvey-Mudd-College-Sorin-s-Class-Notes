
## Definition
We define the Laplace transform of $x(t)$ as
$$
X(s) = \int_{-\infty}^{\infty} x(t)e^{-st}  \, dt
$$

Aside: Where does this definition come from?
We take $e^{st}$ (a function in time with s as some complex number) and pass it through a system with response $h(t)$ to get $y(t)$. This is a convolution in time, so we have
$$
\begin{align}
y(t) & = e^{st}*h(t) \\
	 & = \int_{-\infty}^{\infty}h(t)e^{s(t-\tau)}  \, d\tau \\
 & = e^{st} \underbrace{ \int_{-\infty}^{\infty} h(\tau)e^{-s\tau} \, d\tau }_{ H(s) }  
\end{align}
$$
What comes out from this function is just a constant scaling factor times the input - so this is an eigenfunction.

## How to calculate
There are two methods we could use. 

### Manually 
You can always just plug and chug, manually computing. However, this is time consuming and somewhat difficult.
Lets see examples of where this is tricky:
#### Ex 1: $e^{-at}u(t)$
$$
\begin{align}
x(t)  & = e^{-at}u(t),  & a > 0 \\
X(s) & = \int_{-\infty}^{\infty} x(t)e^{-st} \, dt \\
X(s)  & = \int_{0}^{\infty} e^{-(s+a)t} \, dt \\
  & = -\frac{1}{s+a} e^{-(s+a)t} \big|_{0}^\infty
\end{align}
$$
For this to converge, it requires $s+a$ to have a positive real component. 
$$
\begin{align}
X(s) &  = -\frac{1}{s+a} [0-1] \text{when} \mathrm{Re}\left\{ s \right\} +a > 0 \\
 & = \frac{1}{s+a}
\end{align}
$$
We have
$$
e^{-at}u(t) \overbrace{ \leftrightarrow }^{ \mathscr{L} } \frac{1}{s+a}
$$


#### Ex 2: $-e^{-at}u(-t)$
$$
\begin{align}
X(s) & = \int_{-\infty}^{\infty}  x(t) e^{-st} \\
 & = \int_{-inf}^{0} -e^{-(s+a)t} \, dt \\
  & = \frac{1}{s+a}e^{-(s+a)t}dt \big|_{-\infty}^0\\
  & = \frac{1}{s+a}[1-0]  & \text{when } \mathrm{Re} \left\{ s \right\} +a < 0 \\
-e^{-at}u(-t)  & \overbrace{\leftrightarrow}^{\mathscr{L}}  \frac{1}{s+a}
\end{align}
$$


#### Ex 3: $x(t)=\cos(\omega_{0}t)u(t)$

![[IMG_2EA59245E87F-1.jpeg|500]]
$$
\begin{align}
 X(s)& = \frac{1}{2} \frac{s+j\omega_{0}+s-j\omega_{0}}{(s-j\omega_{0})(s+j\omega_{0})} \\
 & = \frac{s}{s^{2}+\omega_{0}^{2}},  & \mathrm{Re}\left\{ s \right\} >0
\end{align}
$$

## Use a look up table you dolt.

There are several nice properties of the Laplace transform, and some other poor bloke had to manually calculate. It doesn't always work, but if you can break apart your expression into nice terms (i.e. partial fraction decomposition) then you have something easily workable.

The main thing to look out for is the region of convergence. For instance, when adding or convolving two signals, the properties only hold if convolving, you have $R_{1} \cap R_{2}$.

Lets do an example:
$x(t)  = \delta(t) + \frac{1}{2}e^{2t}u(t) - 2\cos (\omega_{0}t )u(t)$

We can break this into a bunch of linearly adding terms:

$$
\begin{align}

\delta(t)  & \leftrightarrow 1, \text{all s} \\
\frac{1}{2}e^{2t} u(t)  & \leftrightarrow \frac{1}{2} \frac{1}{s-2}, Re \left\{ s \right\} > 2 \\
-2 \cos(\omega_{0}t)u(t)  & \leftrightarrow -2 \frac{s}{s^{2}+\omega_{0}^{2}}, \mathrm{Re}\left\{ s \right\} > 0 \\

\end{align}
$$
$$
X(s) = 1+ \frac{1}{2} \frac{1}{s-2} - 2 \frac{s}{s^{2}+\omega_{0}^{2}}, \mathrm{Re}\left\{  s \right\}>2
$$
Note the convergence condition: This is the intersection between the regions of convergence from all other sets. Please god let there be an intersection always. Otherwise you have bad system design.

(am I being too snarky in these notes? I'm normally quite serious)


