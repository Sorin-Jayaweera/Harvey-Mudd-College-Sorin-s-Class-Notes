Inductance

Lets take a circuit and calculate the back emf (arising from self inductance).
$\boxed{\epsilon_{induced}=L\left| \frac{di}{dt} \right|}$
We can get here by:
$$
\begin{align}
E=-\frac{d}{dt} \Phi_{b} \\
\Phi_{b}=\iint\vec{B}\cdot \vec{dA} \\
=i \iiint \frac{\mu_{0}}{4\pi} \frac{\vec{dl} \times  \vec{r}}{r^{2}} dA \\
\text{ this is gross, so we call this } \iiint \text{  = L } \\
\Phi_{b}=iL \\
E=L \left| -\frac{d}{dt} i \right| 
\end{align}
$$

Lets calculate L for a solenoid.

There are $n$ loops per distance $x$ in a solenoid, so the flux enclosed by the 1d wire (stretched out to be the 3d cylinder) is $\Phi_{b}=\text{ length * n} \times \iint_{\text{ loop }}\vec{B}\cdot \vec{dA}$ 
$$
\begin{align}
\Phi_{b} & =(nl)(B\pi r_{s}^{2}) \\
 & = \mu_{0}n^{2}i\pi r_{s}^{2}l \\
\text{ So we get  } \epsilon  & = -L \frac{d}{dt} i  \\
 & =\mu_{0}n^{2}\pi r_{s}^{2}L \frac{d}{dt} i \\

\end{align}
$$
$\boxed{L = \mu_{0}n^{2}\pi r_{s}^{2}L}$

inductance $L$ is measured in units $\frac{[V]}{\left[ \frac{A}{S} \right]}=\frac{VS}{A}$
![[Pasted image 20241022101950.png]]


## Energy in B fields
$\frac{dw}{dt}=\text{ Power }$
$$
\begin{align}
[P]=\frac{j}{s} \\
[V]=\frac{J}{c} \\
[i]=\frac{c}{s} \\
\end{align}
$$
So $P=i\Delta v$.
What is the work to "charge up" and inductor?

$$
\begin{align}
W=\int Pdt = \int  \left( iL \frac{di}{dt} \right) dt \\
W=\frac{1}{2}Li^{2}
\end{align}
$$


Inductor equations:
$$
\boxed{
\begin{align}
\left| E \right| =L\left| \frac{d}{dt} i \right|  \\
\text{ Energy stored: } \\
\mathbb{U_{b}}^{}=\frac{1}{2}Li^{2} \\
\text{ Energy density: } \\
U_{b} = \frac{1}{2} \frac{B^{2}}{\mu_{0}}
\end{align}
}
$$
