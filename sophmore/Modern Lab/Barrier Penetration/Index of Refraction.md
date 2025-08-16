We must find the index of refraction of our material, polyethylene. 

## Theory

The index of refraction of our material can be found using Snell's law. 


$$
\begin{align}
\frac{n_{\text{ poly }} }{n_{air} } \equiv \frac{\sin\theta_{i}}{\sin\theta_{r} } 
\end{align}
$$

where $\theta_{i}$ is the incident angle and $\sin\theta_{r}$ is the reflected angle. $N_{air}\approx 1$.

In the diagram below. we position our transmitter at the left position at angle $\psi$, and our receiver on the right side at angle $\psi$. The angle that has the maximum transmission will read the largest value.

We can rewrite this definition in terms of experimental parameters:
![[Pasted image 20250414212510.png]]
With geometry, we can define an angle $\psi$ off of $\frac{\alpha}{2}$. We use the line perpendicular to $\frac{\alpha}{2}$ as our reference for $0$ deg $\phi$, as this way a small error  in our angle is relatively smaller, as long as we know $\frac{\alpha}{2}$ to high precision. In our setup, $\alpha \approx \frac{\pi}{2}$. 

Therefore, we have
$$
\begin{align}
n \equiv \frac{\sin\left( \psi+\frac{\pi}{4} \right)}{\sin\left( \frac{\pi}{4 } \right)}
\end{align}
$$
We can now measure our maximum transmission angle of incidence and use it to define our $n$ for the material.


## Experiment
We position our transmitter and receiver at incremental $\psi$ to find the rough location where we get the greatest transmission. See Table 3 for a summary of the results.
We found the greatest intensity at $\theta= 13$ degrees, which gives us:

$n=1.52\pm 0.03$



Table 3:

|                     |                  |       |
| ------------------- | ---------------- | ----- |
| Index of Refraction | 10x reading      |       |
| Psi                 | Receiver Reading | Error |
| 0                   | 0.1              | 0.025 |
| 5                   | 0.37             | 0.025 |
| 10                  | 0.7              | 0.025 |
| 15                  | 0.82             | 0.025 |
| 20                  | 0.75             | 0.025 |
| 17                  | 0.8              | 0.025 |
| 16                  | 0.81             | 0.025 |
| 14                  | 0.85             | 0.025 |
| 13                  | 0.88             | 0.025 |
| 12                  | 0.82             | 0.025 |