## Fundamentals of signals
### Continuous Time
A CT (continuous time) function is periodontic if it repeats itself after a time T
$$
\begin{align}
X(t)= x(t+T)
\end{align}
$$
This is a boundary condition. 

$$
\begin{align}
A\cos(\omega_{0}t+\phi ) = A\cos(\omega_{0}(t+T)+\phi) \\
A\cos(\omega_{0}t+\phi+\underbrace{ \omega_{0}T }_{ 2\pi })
\end{align}
$$
This $\omega_{0}T$ that gets the function is the fundamental frequency that gets it to repeat. 
$$
\begin{align}
\omega_{0}T = 2n\pi, \, \, n = \pm 1, \pm 2\dots \\
\end{align}
$$
Where the fundamental period is $T_{0}=\frac{2\pi}{\omega_{0}}$

Lets look at two frequencies added together. What is the fundamental period?

$$
\begin{align}
x(t) = A\cos(\underbrace{ 2\pi  }_{ \omega_{0}^{a} }t+\phi_{a} ) + B\cos(\underbrace{ 3\pi }_{ \omega_{0}^{b} }t+\phi)
\end{align}
$$

$$
\begin{align}
T_{0}= \frac{2\pi n_{a}}{2\pi} = \frac{2\pi nb}{3\pi} 
\end{align}
$$
We have to have
$T_{0}= n_{a}= \frac{2}{3}n_{b}$ at the same time.
This represents how many "cycles" it takes for each function to repeat. 
The smallest number for this is $n_{a}=2, m_{b}=3$. 
This means $T_{0}=2$. The fundamental frequency is where the *overall* pattern is repeating. 

There are some sums of signals that could *never* be periodic.
For the signals to sync up,
$\frac{n_{a}}{n_{b}}$ has to be rational, so $\frac{\omega_{0}^{a}}{\omega_{0}^{b}}$ would be rational. If one of the $\omega_{0}$s are irrational, i.e. $\pi$, then the sinusoids would NEVER line up perfectly. Weird but cool!

Also, note that a time shift corresponds to a phase shift.
$$
\begin{align}
A\cos(\omega_{0}(t+t_{0})+\phi) = A\cos(\omega_{0}t + \underbrace{ (\omega_{0}t_{0}+\phi) }_{ \phi' })
\end{align}
$$
$\phi'=\phi+\Delta \phi$, $\Delta \phi=\omega_{0}t_{0}$.

A phase shift could also be expressed as a time shift:

$$
\begin{align}
A\cos(\omega_{0}t + \phi) = a\cos(\omega(t+\Delta t) ) \\
\Delta t = \frac{\phi}{\omega_{0}}
\end{align}
$$
We're just manipulating the expression. Phase and time shifts are the same. 

Now lets move to discrete time.
The frequency 

### Discrete Time
Lets start with continuous time.
$x(t)= A\cos(\omega_{0}t+\phi)$.
We'll sample this at $T$, the sampling period. 

We'll make a discrete signal by
$$
\begin{align}
x[n] = A\cos(\omega_{0}nT+\phi)
\end{align}
$$
which is equal to $x(nT)$.
We can define a *dimensionless frequency*, $\hat{\omega}_{0} = \omega_{0}T$. 
$$
\begin{align}
x[n] = A\cos(\hat{\omega_{0}}n+\phi) \\
\end{align}
$$
n is an integer without units of time, so the frequency must also be dimensionless.


### Differences
Lets look at other distinctions between CT and DT.

#### Time and Phase Shifts
A "time" shift in DT is shifting by $n$, a integer. 
$$
\begin{align}
x[n]  & = A\cos(\hat{\omega_{0}}(n+n_{0})+\phi) \\
 & = A\cos(\hat{\omega}_{0} n + \underbrace{ \hat{\omega_{0}}n_{0}+\phi }_{ \phi' }) \\
 & =A \cos(\hat{\omega_{0}}n + \phi')
\end{align}
$$
Can we go the other way?
A time shift is the same as a phase shift.
Are all phase shifts expressible as time shifts?
no! 
We can only represent phase shifts that are capturable by integer multiples of $\hat{\omega_{0}}$. 
$$
\begin{align}
\Delta \phi = \hat{\omega_{0}}n_{0}
\end{align}
$$
We can only have phase shifts that are multiples of $\hat{\omega_{0}}$ because $n$ is an integer.

again: Only phase shifts that are integer multiples of $\hat{\omega}_{0}$.


#### Periodicity
$$
\begin{align}
x[n] = x[n+N]
\end{align}
$$
We have a condition on $N$.
$$
\begin{align}
A\cos(\hat{\omega_{0}}n)  & = A\cos(\hat{\omega_{0}}(n+N)) \\
 & = A\cos(\hat{\omega_{0}}n + \hat{\omega_{0}}N + \phi)
\end{align}
$$
which means $\hat{\omega}_{0}N=2\pi m$. 
Lets take $\hat{\omega_{0}}=2$, then $n=\pi m\implies \frac{n}{m}=\pi$. So.... not every DT sinusoid is periodic.

Every periodic function (not those irrational edge cases) has a Fundamental period $N_{0}$.
$$
\begin{align}
x[n] = A\cos\left( \underbrace{ \frac{4\pi}{41} }_{ \hat{\omega}_{0} }n \right) \\
N = \frac{2\pi m}{\frac{4\pi}{41}} = \frac{41m}{2}
\end{align}
$$
We can pick $m=2$, $N=41$.
so $N_{0}=41$, the smallest $N$ for which this is true (where $n \text{ and }  m$ are integers).

What if we have something else:
$$
\begin{align}
x[n] = A\cos\left( \frac{n}{6} \right) \\
N = \frac{2\pi m}{\hat{\omega_{0}}} = \frac{2\pi m}{6} = \frac{\pi m}{3}
\end{align}
$$
Uh...
$n = \frac{\pi}{3}m$... but $n \text{ and } m$ must be integers, so this isn't possible. This signal isn't periodic!

One more example
![[20250828_103247.jpg]]
We see that plugging in $N_{0}=20$ gets us $8\pi$ and $6\pi$, which are both multiples of $2\pi$, so that's when these two line up.


 For continuous time, different fundamental frequencies are not the same signal.  But for discrete time, what if $\hat{\omega_{2}} = \hat{\omega_{1}} + \underbrace{ 2\pi m }_{ integer }$
![[Pasted image 20250828103833.png]]


Lets compare 


|                            | CT                         | DT                                                                      |
| -------------------------- | -------------------------- | ----------------------------------------------------------------------- |
| Dimensions of $\omega_{0}$ | rad/s                      | rad                                                                     |
| Timeshifts                 | Time shift <-> Phase shift | Timeshift -> Phase shift                                                |
| Distinct signals           | Yes                        | Identical in some cases when $\hat{\omega_{2}}=\hat{\omega_{1}}+2\pi m$ |
| Periodicity                | always                     | not always                                                              |
|                            |                            |                                                                         |

### Real exponentials

#### CT
$$
\begin{align}
x_{t} = Ce^{at} \, \, -\infty < t < \infty \\
\end{align}
$$

#### DT
$x[n]=C^{Bn}= C \alpha^{n}$

We can have exponential growth or decay depending on $\alpha< \text{ or } > 1$.

### Complex Exponentials
CT:
