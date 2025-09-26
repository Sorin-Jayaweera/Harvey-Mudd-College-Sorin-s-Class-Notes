$$
\begin{align}
\chi^{2}= \sum_{n=0}^{N-1} \frac{(y_{n} -E_{n})^{2}}{E_{n}}
\end{align}
$$


## Monte Carlo Integration

To calculate pi,
randomly put darts around a unit square. Count the number that are within a radius out of the area of the square. 

How should the accuracy of this method scale with the number of darts? 

we have $P =\text{ probability of success }, \text{ and } q = \text{ probability of failure }$.
$q=1-p$
for each throw we have
$(p+q)^{n}$ which we can expand with the binomial expansion
$$
\begin{align}
p^{n}+ {n\choose  1} p^{n-1}q + \dots 
\end{align}
$$
$$
\begin{align}
\bar{N}_{succ} = Np \\
\sigma = \sqrt[]{ Npq }  
\end{align}
$$
## Approximating the volume of a hypersphere
$$
\begin{align}
V = C_{d} R^{d} \\
C_{d} = \frac{\pi^{d/2}}{\frac{d}{2} \gamma\left( \frac{d}{2} \right)} 
\end{align}
$$
For 