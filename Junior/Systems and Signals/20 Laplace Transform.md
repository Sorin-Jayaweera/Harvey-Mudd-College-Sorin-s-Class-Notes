
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

### Use a look up table you dolt.

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


## Inverse Laplace
We have two methods:

### Contour Integration
No one remembers how to do this
$$
x(t) = \frac{1}{2\pi j}\int_{\sigma=-j \infty}^{j \infty}  X(s)e^{st}\, ds 
$$

### Again, just give up and use a look up table 
We can usually do partial fraction expansion.

#### Step 1: Prep H(s) for decomposition
The first step is to make sure that $H(s)$ is bottom heavy.
For instance,
$$
\begin{align}
\frac{1}{s+2} ,& \frac{2s+3}{s^{2}+4s+1}
\end{align}
$$
The order in the denominator must be higher than in the numerator (not the same).

If this is not true, then divide out using long division. 
$$
\frac{s^{3}}{s^{2}+1} = s - \frac{s}{s^{2}+1}
$$
Or another,
$$
\frac{s^{2}+2}{s^{2}+2s+1} = 1 + \frac{-2s+1}{s^{2}+2s+1}
$$

#### determine denominator factors

For first order terms, we can easily pull out. I.e.
$$
\frac{3s+2}{(s+3)(s+2)} = \frac{A}{s+3} + \frac{B}{s+2}
$$
For second order terms, we need
$$
\frac{s^{2}}{(s+1)(s^{2}+4s+1)} = \frac{A}{s+1} + \frac{Bs+C}{s^{2}+4s+1}
$$
And so on for higher order.

For repeated terms, we have each count for powers of that thing:
$$
\frac{3s+1}{s^{3}(s+1)^{2}} = \frac{A}{s} + \frac{B}{s^{2}} + \frac{C}{s^{3}} + \frac{D}{s+1} + \frac{E}{s^{2}+1}
$$

#### Solve the numerator coefficients
We have to satisfy the equality, so make a system of equations.
$$
\begin{align}
A(s^{2}+1)+ (Bs+C)s = 2s^{2}+s+1\\
(A+B)s^{2}+Cs+A = 2s^{2}+s+1 \\
A+B = 2, C=1, A=1, B=1
\end{align}
$$


## Convergence
Take
$$
\begin{align}
X(s) & = \frac{A}{s+2} + \frac{B}{s+1}
\end{align}
$$
if $\mathrm{Re}\{s\}=-2$ or $\mathrm{Re}\{s\}=-1$, this will explode. The region of convergence doesn't include these two points. The sum will converge at the intersection of those two, so $\mathrm{Re}\{s\}\text{ must be }>-1$. 

Lets take another example.

$$
\begin{align}
X(s)  & = \frac{s+4}{s^{2}+4s+5} \\

\end{align}
$$
This would break down into
$s=-2-i$ and $s=-2+i$, which isn't nice.
However, we have some identities we could use:
$$
\begin{align}
e^{-at}\cos(\omega_{0}t)  & \leftrightarrow   \frac{s+a}{(s+a)^{2}+\omega_{0}^{2}} & \mathrm{Re}\left\{ s \right\} >-a\\
e^{-at}\sin(\omega_{0}t)  & \leftrightarrow   \frac{\omega_{0}}{(s+a)^{2}+\omega_{0}^{2}} & \mathrm{Re}\left\{ s \right\} > -a \\
e^{-at}u(t)  & \leftrightarrow  \frac{1}{s+a} & \mathrm{Re}\left\{ s \right\} > -a \\
-e^{-at}u(-t)  & \leftrightarrow   \frac{1}{s+a} & \mathrm{Re}\left\{ s \right\} < -a
\end{align}
$$

We could decompose this $X(s)$ to be
$$
\begin{align}
\frac{s+4}{(s+2)^{2}+1} = \frac{s+2}{(s+2)^{2}+1} + 2 \frac{1}{(s+2)^{2}+1}
\end{align}
$$
This nicely fits the first two, so we get
$$
\begin{align}
x(t) = e^{-2t}\cos(t)u(t) + 2e^{-2t}\sin(t)u(t)
\end{align}
$$

## Interpreting Laplace

### Understanding the region of convergence

We could have the entire s plane, to the left of a line, to the right of a line, or between two segments. Lets think about what is happening in the time domain for these.

#### Entire S plane
This corresponds to a finite length signal that is zero below some $T_{1}$ and above some $T_{2}$.

#### Left half plane
This corresponds to a left sided signal, where the signal can have a value for all times before $T_{1}$ but is zero after.

#### Right half plane

This corresponds to a left sided signal, where the signal is zero for all times before $T_{1}$ but can have any value after.

#### Single strip
A two sided signal that can hold any value anywhere in time.

### Example
$$
\begin{align}
x(s) = \frac{s^{2}+1}{(s-1)(s+1)(s+3)}
\end{align}
$$
The numerator will be zero for $s=\pm i$

We have poles at $s=1,s=-1,s=-3$.
The region of convergence can never include a pole. 

Depending on the signal type, we could either have right of 1, left of -3, or between -3 -1 or between -1 and 1





Consider a rational $X(s)$
$$
\begin{align}
\frac{a_{0}s^{m}+ a_{1}s^{m-1}+\dots+a_{m}}{b_{0}s^{n}+b_{1}s ^{n-1} + \dots + b_{n}}
\end{align}
$$
This has the roots
$$
\begin{align}
k\cdot\frac{\Pi^{m}_{i=1} (s-z_{i})}{\Pi_{k=1} ^{n}(s-p_{k} )}
\end{align}
$$

$$
\begin{align}
\left| x(j\omega) \right| = 
\left| k \right| \cdot\frac{\Pi^{m}_{i=1} |s-z_{i}|}{\Pi_{k=1} ^{n}|s-p_{k} |}
\end{align}
$$
The numerator is the distance from zeros, and the denominator is distance from poles.

$$
\begin{align}
\measuredangle  x(j\omega) = \measuredangle  k + \sum_{i=1}^{m} \underbrace{ \measuredangle  (j\omega-z_{i}) }_{ \text{ angle from zeros } } - \sum_{k=1}^{n} \underbrace{ \measuredangle  (j\omega -p_{k}) }_{ \text{ angle from pole } }
\end{align}
$$

These will help us develop filters for our data.

### Example

$$
\begin{align}
X(s) = \frac{2}{s+2}, \mathrm{Re}\left\{ s \right\} > -2
\end{align}
$$
The magnitude is
$$
\begin{align}
\left| X(j\omega) \right|  & = \frac{2}{\left| j\omega-(-2) \right| } \\
 & = \frac{2}{\text{ distance from }j\omega \text{ and }  2}
\end{align}
$$
And the angle is
$$
\begin{align}
\measuredangle   X(j\omega)  & =\measuredangle  2 - \measuredangle  (j\omega-(-2)) \\
 & = -\measuredangle  (j\omega-(-2))
\end{align}
$$

![[Pasted image 20251111105132.png|500]]

