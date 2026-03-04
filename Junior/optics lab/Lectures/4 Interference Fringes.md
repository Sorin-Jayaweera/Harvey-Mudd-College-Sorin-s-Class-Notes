$\tau$ is controlled by the path length difference. 

phase shift is $\omega \tau$. 

Autocorrelation: How something relates to itself, i.e. how a wave relates to how it was at the source vs how it is after a shift $\tau$.


$$
\begin{align}
g^{(1)}(\tau) = \frac{\left< E^{+}(t+\tau)E^{-}(t) \right> }{\left< E^{+}(t)E^{-}(t) \right> }
\end{align}
$$
We have properties of this
$$
\begin{align}
g^{(1)}(-\tau) = [g^{(1)}(\tau)]^{*} 
\end{align}
$$
We can rewrite that as
$$
\begin{align}
 & \left< E^{+}(t-\tau+\tau)E^{-}(t) \right>  \\ & 
= \left< E^{-}(t-\tau)E^{+}(\underbrace{ t-\tau }_{ t' }) \right>  \\
 & = \left< E^{-}(t'+\tau)E^{+}(t') \right> 
\end{align}
$$
The reference shift doesn't matter because we're time averaging. These are juts complex conjugates of each other. 


## LIGHT SOURCE WITH 2 FREQUENCIES

$$
\begin{align}
E^{+}(t)= E_{1}^{+} e^{-i\omega_{1}t}+ E_{2}^{+}e^{-i\omega_{2}t}
\end{align}
$$
lets simplify and say $E_{1}=E_{2}=E_{0}$ for now to be nice. 

What is the input intensity?
$$
\begin{align}
I_{\text{ in }}  & = \frac{2}{\mu_{0}c}\left< E^{+}(t)E^{-}(t) \right>  \\
 & = \frac{2}{\mu_{0}c}\left< E_{1}^{+}e^{-i\omega_{1}t}E_{1}^{-}e^{i\omega_{1}t}E_{1}^{+}+E_{2}e^{-i\omega_{2}t}E_{2}^{-}e^{i\omega_{2}t} + E_{1}^{+}e^{-i\omega_{1}t}E_{2}^{-}e^{+i\omega_{2}t}+ E_{2}^{+}e^{-i\omega_{2}t}E_{1}^{-}e^{+i\omega_{1}t}\right>   \\
& = \frac{2}{\mu_{0}c}\left< E^{+}_{1}E^{-}_{1}+E^{+}_{2}E^{-}_{2}+ E_{1}^{+}E_{2}^{-}e^{i(\omega_{2}-\omega_{1})t}+E_{1}^{-}E_{2}^{+}e^{i(\omega_{1}-\omega_{2})t}   \right> 
\end{align}
$$

The first two have the $e^{i\omega_{n}t}e^{-i\omega _{n}t}$ cancel out. The rest are time varying as
$$
\begin{align}
e^{\pm i(\omega_{1}-\omega_{2})t }
\end{align}
$$
The time average depends on how long we're averaging over. 

If we have a detector with an averaging time more than a nanosecond, the time average is effectively zero. $T_{\text{ detector minimum }}$

What kinds of frequency differences make $\left< e^{i(\omega_{1}-\omega_{2})t} \right>$ roughly equal to 0?

$$
\begin{align}
(\omega_{1}-\omega_{2})\gg \frac{2\pi}{T_{\text{ det,min }} } = \frac{2\pi}{10^{-9}s} \\
\nu_{1}-\nu_{2} \gg  10^{9}Hz
\end{align}
$$

$\nu = \frac{c}{\lambda}$ so we can write
$$
\begin{align}
\frac{c}{\lambda_{1}} - \frac{c}{\lambda_{2}} \gg  10^{9}Hz \\
\frac{(\lambda_{2}-\lambda_{2})c}{\lambda_{1}\lambda_{2}} \gg  10^{9} Hz \\

\end{align}
$$

As long as $\lambda_{2}-\lambda_{1}\gg 10^{-3}$ nm, $\left< e^{\pm i(\omega_{2}-\omega_{1})t} \right>\approx 0$
$$
\begin{align}
I_{in} = \frac{2}{\mu_{0}c}(\left| E_{1} \right|^{2}+\left| E_{2}\right|^{2}  )  \\
I_{\text{ out }} = \frac{1}{2} I_{in} \left< \frac{1- \cos \omega_{1}\tau}{2} + \frac{1- \cos \omega_{2}}{2} \tau\right>   
\end{align}
$$

We define fringe visibility as $\frac{I\text{ out }}{I_{\text{ in }}}$ 
$$
\begin{align}
V(\tau) = \frac{I_{\text{ out,max }}-I_{\text{ out,min }} }{I_{\text{ out,max }}+I_{\text{ out,min }}}
\end{align}
$$

## Many wavelengths
Lets say that we have the sum of a bunch of fields at different frequencies.
if 
$$
\begin{align}
\omega_{j}-\omega_{k} \gg  \frac{2\pi}{T_{\text{ det }} }  
\end{align}
$$
We can get that 
$$
\begin{align}
I_{\text{ in }} = \sum_{j}^{} \frac{2 \left| E_{j}^{+}  \right|^{2} }{\mu_{0}c} = \sum_{j}^{} I_{j} 
\end{align}
$$
