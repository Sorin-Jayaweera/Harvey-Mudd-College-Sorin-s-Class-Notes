There are 2 main concepts that we want to focus on. 
1) The distinction between continuous and discrete signals
2) Fourier Series vs Fourier transforms

There exist all 4 combinations between these two -continuous time Fourier series, a discrete time Fourier series, continuous time Fourier transforms, and discrete time Fourier transforms. 


## Signals
A signal is a function of 1 or more independent variables.
Examples: A pressure wave. Pressure at a position could be a function of time (speaking at a microphone).

We represent signals in the time domain or frequency domain usually (Fourier methods). 

If we know the behavior of basic signals really well, then if a more complex function is a linear combination of them, then the output is a linear combination of the simpler inputs. 

Take two inputs to a linear time invariant system. The outputs are just a combination of the individual function outputs. 
![[Pasted image 20250826100508.png]]

Really, passing any functions of basic signals makes the sum of the outputs on those basic signals. 
$$
\begin{align}
ax_{1}+bx_{2}\implies ay_{1}+by_{2}
\end{align}
$$

### Continuous vs Discrete  Time Signals
We denote continuous time by  $x(t)$, whereas discrete time is $x[t]$. X is not defined if the argument $t$ is not an integer - its a "sample number". 

Think class size by graduation year - there is no 2025.2 graduating class, only at 2024 2025 and 2026 etc...

We worry about discrete time systems because we can't capture the full resolution of life - we represent and store signals in discrete manners by sampling a continuous time signal. 


## Systems
 Systems *process* signals, they're a function or a map from input to output.

Take a spring mass system - input force and output x(t). This is a single input single output system (SISO). Similarly there are systems with multiple inputs and outputs (MIMO) ( two blocks in series on springs  with two output positions).

We'll look at some properties of systems.
### Linearity
The scaling property applies:
$ax\to ay$. 

Superpositions work:
if $x_{1}\to y_{1}, x_{2}\to y_{2}$ then $x_{1}+x_{2}\to y_{1}+y_{2}$

### Time invariance
Delaying an input by T delays generates the same output delayed by T. 

If a rocket is burning fuel, it is not time invariant - mass is changing, etc. LTIs would respond to the same input in the same way no matter the time or area. 

$\phi(t)\to \psi(t)$

$\phi(t_{0}+t)\to \psi(t_{0}+t)$


## Frequency domain
Take a signal in the time domain: $x(t)= A\cos(\omega_{0}t)$.
In the frequency domain, this would be


$x(t) = \frac{A}{2}[e^{j\omega_{0}t}+e^{-j\omega_{0}t}]$
$e^{j\theta}=\cos(\theta)+j\sin(\theta)$
This signal has amplitude $\frac{A}{2}$ at $-\omega_{0}\text{ and } \omega_{0}$


We can also look at sin.
$$
\begin{align}
A\sin(\omega_{0}t) = \frac{A}{2j}(e^{j\omega_{0}t}- e^{-j\omega_{0}t}) \\
\end{align}
$$

We don't really like $j$ on the denominator, so we write

$$
\begin{align}
\frac{1}{j} = \frac{1}{e^{j \frac{\pi}{2}}} = e^{\frac{-j\pi}{2}}
\end{align}
$$

