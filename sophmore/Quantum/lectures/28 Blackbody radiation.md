
>[!abstract]+ Recall: 
>
>Total energy density in a box was
$$
\begin{align} \\
\frac{E_{tot}}{L^{3}} =\frac{ 8 \pi k_{b} ^{4}T^{4}}{c^{3}h^{3}}\underbrace{ \int_{0}^{\infty} \frac{x^{3}}{e^{x}-1} }_{ \frac{\pi^{4}}{15} }\\ 
 \frac{E_{tot}}{L^{3}} \frac{8\pi^{5} k_{b}^{4}T^{4}}{15c^{3}h^{3}}= aT^{4}
\end{align}
$$
> Note: This is only valid if the wavelength is comparable to or smaller than the size of the box. 
> 

We define a new physical concept, the radiancy, and use it to relate our result from a box to the spectrum from stars.

## Blackbody radiation


We draw another hollow conducting box with side lengths $L$ that has a bath of photons inside with different frequencies. Lets put a perfect absorber, a sphere that will absorb every photon that hits it. This is a "blackbody". 

Because it is a perfect absorber, it only emits radiation from its temperature. 

At equilibrium, the temperature of the cavity will be the temperature of the black body, $T=T_{bb}$

This corresponds to the statement that the radiancy $R_{t,inc}=R_{T,\text{ emitted }}$.
The Radiancy $R_{t}(\nu)$ is the $\frac{\text{ power }}{\text{area * frequency }}$. 
$R_{t}(\nu)d\nu$ is $\frac{\text{ power }}{\text{ area }}$.

In short - energy absorbed is energy emitted. 

Lets try to understand the radiancy by cutting a tiny hole in the box and observing the photons that come out. Lets think through the energy per frequency that escapes over a $\Delta t$. 

To escape in a time $\Delta t$, the photons have to be within a radius $c\Delta t$ from the hole. Lets integrate over the surface of this hemisphere around the hole.

$$
\begin{align}
R_{t} (\nu)A\Delta t= \int_{}^{} \rho(\nu)f_{\text{ esc }} dVol
\end{align}
$$

where $f_{esc}$ is a factor that accounts for the direction of the photon. 

Looking at the hole from directly above has basically zero area, where as directly in front of it sees the entire hole, so we need a correction factor for the apparent size of the hole. This factor is $\cos\theta$. 
$$
f_{esc}= \frac{A\cos\theta}{4\pi r^{2}}
$$
For spherical coordinates (since were on a hemisphere),
$$
\begin{align}
dVol = r^{2}\sin\theta d\theta d\phi
\end{align}
$$
We have now

$$
\begin{align}
\int\rho(\nu) \frac{A\cos\theta}{4\pi r^{2}}r^{2}\sin\theta dr d\theta d\phi \\
R_{t} (\nu)= \frac{\rho(\nu)A}{4\pi A\Delta t} \int_{0}^{c\Delta t} dr \int_{0}^{2\pi}d\phi \int_{0}^{\frac{\pi}{2} }d\theta \sin\theta \cos\theta \\
= \frac{c\rho}{2}\left[ \frac{1}{2} \sin ^{2}\theta \right] \bigg|_{0}^{\frac{\pi}{2}} \\
= \frac{c}{r}\rho(\nu)  
\end{align}
$$

The punchline: The radiancy is proportional to the Planck function that we derived last lecture. The radiancy absorbed by the blackbody and to the radiancy emitted by the blackbody. 

To reiterate: We had a box and an ideal equilibrium to relate the incoming radiation from a box onto a blackbody, and argue that the spectrum leaving the box from our hole is the same as the spectrum that is being absorbed and emitted by the blackbody. The only thing that matters is the temperature. The spectrum inside the box is the spectrum outside the box. 

From this, we can extrapolate - the spectrum of cavity radiation is also the spectrum of radiation of any black body.


## Stephan-Boltzman Law $F=\sigma T^{4}$
We do exactly the same integral,
$$
\begin{align}
F= \int_{0}^{\infty} R_{t} (\nu)d\nu = \frac{c}{4} \int_{0}^{\infty} \rho(\nu)d\nu = \frac{ca}{4}T^{4}
\end{align}
$$
where $a=\frac{8\pi^{5}k_{b}^{4}}{15c^{3}h^{3}}$.

We define the Stephan-Bolzmann constant
$$
\begin{align}
\sigma = 5.678 \times  10^{-8} \frac{J}{sm^{2}k^{4}}
\end{align}
$$

So the Power is 
$$
\begin{align}
P = \sigma T^{4} \underbrace{ A }_{ \text{ area of whatever thing } }
\end{align}
$$

## Incandescent Lightbulb
Imagine a tightly would piece of metal. Usually these are on the order of 1cm, but are so tightly wound that its actually about 1 meter long.

We can unroll it to a height $\pi h$ and a length $L$.

$$
\begin{align}
P & =\sigma T^{4}A \\
 & =\sigma T^{4} (\pi hL) \\
T = \left( \frac{P}{\sigma \pi hL} \right)^{\frac{1}{4}} = 4000K
\end{align}
$$
Lower temperature gives a lower spectrum. The peak spectrum from this bulb is far in the infrared - $\lambda_{max}=1.45\mu m$, so we can't even see most of it. Plus a ton is lost to heat.
![[Pasted image 20250404104125.png]]

Lets do another example, and find the temperature equilibrium of the earth. 

For earth's equilibrium, the energy absorbed is related to its radiation.

$P_{abs}= P_{em}$

We have an effective cross sectional area of the earth that is seen by the light, the distribution of the power over the massive sphere at the radius, a term for the albedo of the earth where more stuff is reflected (absorption = 1-albedo). 

$$
\begin{align}
P_{s}  \cdot \frac{\pi R_{e} ^{2}}{4\pi d^{2}} \cdot f_{abs} = \sigma T_{e} ^{4} \cdot (r\pi R_{e} ^{2})  \\
4\pi R_{s} ^{2} \sigma T^{4} \frac{\pi R_{e}^{2}}{4\pi d^{2}} f_{ab s} = \sigma T_{E} ^{4}4\pi R_{e} ^{2} \\
T_{e} ^{4} = T_{s} ^{4} \frac{R_{s} ^{2}}{4d^{2}} f_{abs}  \\
T_{e} = T_{s} \sqrt[]{ \frac{R_{s}}{2d}  }   \underbrace{ f_{ab s} }_{ 0.7 }^{\frac{1}{4} } \\
\approx 256 k
\end{align}
$$

We ignored the atmosphere! If we didn't have one, that would be the temperature of the earth! Nice chilly arctic day everywhere. 

![[Pasted image 20250404104248.png]]


The universe is a massive cavity at some temperature. This gives us the cosmic microwave background!

For the first 400,000 years there was a soup of radiation. Eventually atoms started to form, there was a decoupling. Photons had a temperature of 3000 kelvin, so the temperature associated with those photons is now about 2.72545 + 0.00057 K. This is the temperature of outer space.  (Note - we can get colder on earth, which is bonkers). 

We can represent the CMB with spherical harmonics! 