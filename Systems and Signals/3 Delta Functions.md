## Complex Exponentials


### CT
$x(t)- ce^{at}\implies x(t)=\left| c \right|e^{r t}\bigg[\cos(\theta + \omega t) + j \sin(\theta+\omega t)  \bigg]$
$c = ke^{j\theta}$
$a = r+j\omega_{0}$

This R is an envelope that contains the signal

![[Pasted image 20250902094555.png]]

### Discrete time
$$
\begin{align}
x[n] = c \alpha^{n} \\
c' = \left| c \right| e^{j\theta}\\
\alpha'= \left| \alpha \right| e^{j \hat{\omega_{0}}}
\end{align}
$$
$$
\begin{align}
 x[n]  & = \left| c \right| e^{j\theta}(\left|  \alpha \right| e^{j \widehat{\omega}_{0} })  \\
 & = \left| c \right| \left| \alpha \right|^{n}e^{j(\widehat{\omega}_{0} n+\phi)} \\
 & = \left| c \right| \left| \alpha \right| ^{n}(\cos(\widehat{\omega}_{0}n + e) + j\sin(\widehat{\omega}_{0} n+\phi)) 
\end{align}
$$
Where alpha determines the stability of the system.
$$
\begin{align}
 & \left| \alpha \right| = 1 \implies \text{ sines and cosines } \\
 & \left| \alpha \right| >1 \implies \text{ unstable } \\
 & \left| \alpha \right| < 1 \implies \text{ stable }
\end{align}
$$

## Discrete Time Unit Impulse
### Impulse
We hate a discrete delta function
$$
\begin{align}
\delta [n-k] = \begin{cases}
1 & n=k \\
0 & \text{ else }
\end{cases}
\end{align}
$$
For an arbitrary $x[n]$, we isolate a single point by writing
$$
\begin{align}
x[n]\delta[n-k]=x[k]\delta[n-k]
\end{align}
$$


### Unit Step

This is just a sum of impulses to kick on when you want
$$
\begin{align}
u[n] = \sum_{m=0}^{n} \delta[m]
\end{align}
$$
or a nice straight line to the function
$$
\begin{align}
u_{\Delta } (t) = \begin{cases}
0 & t<0 \\
\frac{1}{\Delta}t & 0\leq t\leq \Delta  \\
1  & t > \Delta
\end{cases}
\end{align}
$$
where $\Delta$ is the rising time of the function from the delta. 


We can define a continuous time unit impulse
$$
\begin{align}
\delta_{\Delta} (t) = \frac{d}{dt} (u_{\Delta} t) = \begin{cases}
0 & t < 0 \\
\frac{1}{\delta}  & 0\leq t\leq \Delta \\
0 & t > \Delta
\end{cases}
\end{align}
$$
This always has area 1, since its a rectangle with height $\frac{1}{\Delta}$ and length $\Delta$. 


A continuous delta function is the limit as this rectangle goes to infinite height and zero width. We can look at it like the derivative of the unit step, since that will have infinite slope at the step but zero else where.
$$
\begin{align}
\delta(t) = \frac{ d u(t)}{d t } 
\end{align}
$$

