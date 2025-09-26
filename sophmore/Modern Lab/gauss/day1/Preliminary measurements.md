
## Some theory of note for this section of our experiment:
We want to find the value of I given by
$$
\begin{align}
B_{coil} = \frac{\mu_{0} N i}{2R}
\end{align}
$$
Where $\mu_{0}$ is a $4\pi *10^{-7} \frac{kg M}{A^{2}s^{2}}$, $N$ is the number of turns, $R$ is the radius of the coil, and $i$ is the current flowing through the wire in Amperes, and $B_{coil}$ is the magnitude of the magnetic field produced.

For this, we will find $B_{coil}$ by using a bar magnet. 

Useful properties of a bar magnet: 
For a bar magnet, we have an approximation of two magnetic monopoles, given by 
$$
\begin{align}
B_{ba r}= \frac{\mu_{0}}{4\pi} \frac{2Mr}{(r^{2}-b^{2})^{2}} 
\end{align}
$$
Where $M=2pb$ is the magnetic dipole moment, and $p$ is the monopole strength. 


With the current turned off, the angle of deflection $\phi$ is given by
$$
\begin{align}
\tan(\phi)= \frac{B_{bar}}{B_{h} } 
\end{align}
$$
We can combine this with the earlier expression to get
$$
\begin{align}
\frac{M}{B_{h} }= \frac{2\pi}{\mu_{0}}r^{3}\left( 1- \frac{b^{2}}{r^{2}} \right)\tan \phi
\end{align}
$$

## Experiment

We begin a constant current (313 mA, 16.0 V) flowing through the wires in the positive direction, with minimal nearby magnetic sources. Those nearby should be roughly constant throughout the experiment, and measure the deflection to be 39 degrees, moving clockwise from top down perspective. Bar magnet #6 had to be 33.1 centimeters away to deflect the needle back to its centered position. With the current turned off, the magnet produces a deflection of -39 (we wanted to double check).

With the current off, we measured the angle of deflection caused by the magnet at various distances (given in cm). This produces the following table:

|                  |          |                        |
| ---------------- | -------- | ---------------------- |
| Length of magnet | mu_0     | b (half length magnet) |
| 6.4              | 1.26E-06 | 2.25                   |

|   |   |   |   |   |
|---|---|---|---|---|
|Distance on scale|Distance (cm)|Angle of deflection (deg)|Tan phi|M/B|
||inf|0|0.00|#VALUE!|
|0|50|3|0.05|1.21E+07|
|10|40|4|0.07|2.10E+07|
|20|30|8|0.14|5.79E+07|
|30|20|36|0.73|4.58E+08|
|34.3|15.7|45|1.00|8.08E+08|
|40|10|75|3.73|4.76E+09|
|30.8|19.2|30|0.58|3.80E+08|
|27.3|22.7|20|0.36|2.01E+08|
|17.3|32.7|10|0.18|6.62E+07|

|             |          |
| ----------- | -------- |
| Min M/B     | 4.76E+09 |
| Max M/B     | 1.21E+07 |
| Average M/B | 7.52E+08 |
