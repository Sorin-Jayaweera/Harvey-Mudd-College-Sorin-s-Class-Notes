![[Pasted image 20260207140416.png]]

$\tau$ is the difference in phase shift from each of the two paths. Assuming that overall phase is irrelevant, the total shift $\tau$ can be put onto one path. The difference in length, then, is what matters. The wave travels an extra distance $\mathscr{l}_{2}-\mathscr{l}_{1}$ at a speed $c$ on one way down the arm. The beams have to travel the arm lengths twice - going out to the mirror and back, so it takes time $\frac{2(l_{2}-l_{1})}{c}$ extra to travel the second path. 

![[Pasted image 20260207140429.png]]
We know that

$$
\begin{align}
\tau=  \frac{2(l_{1}-l_{2})}{c}
\end{align}
$$

The phase shift is $\omega \tau$. 

![[Pasted image 20260207155625.png|400]]

$$
\begin{align}
I_{\text{ out }} = \frac{1}{2} I_{in}[1- Re g^{(1)}(t) ] 
\end{align}
$$


We can calculate the coherence function for this
$$
\begin{align}
\left< E^{(+)}(t)E^{(-)}(t) \right> =  E^{(+)}E^{(-)} = E_{1}^{2}+E_{2}^{2}  
\end{align}
$$

We also have
$$
\begin{align}
\left< E^{(+)}(t+\tau)E^{(-)}(t)\right> =  (E_{1}^{(+)}E_{1}^{(-)}e^{-i\omega_{1}\tau}+E_{2}^{(+)}E_{2}^{(-)}e^{-i\omega_{2}\tau})
\end{align}
$$

This gives
$$
\begin{align}
g^{(1)}(\tau) = \frac{(E_{1}^{(+)}E_{1}^{(-)}e^{-i\omega_{1}\tau}+E_{2}^{(+)}E_{2}^{(-)}e^{-i\omega_{2}\tau})}{E_{1}^{2}+E_{2}^{2}   }
\end{align}
$$



We can find 
$$
\begin{align}
Re(g^{(1)}(\tau)) = \frac{E_{1}^{(+)}E_{1}^{(-)}\cos(\omega_{1}\tau)+E_{2}^{(+)}E_{2}^{(-)}\cos(\omega_{2}\tau)}{E_{1}^{2}+E_{2}^{2}}
\end{align}
$$



We can also find
$$
\begin{align}
I_{\text{ in }}  & = \frac{2}{\mu_{0}c}\left< E^{+}(t)E^{-}(t) \right>  \\
 & = \frac{2}{\mu_{0}c}\left< E_{1}^{+}e^{-i\omega_{1}t}E_{1}^{-}e^{i\omega_{1}t}E_{1}^{+}+E_{2}e^{-i\omega_{2}t}E_{2}^{-}e^{i\omega_{2}t} + E_{1}^{+}e^{-i\omega_{1}t}E_{2}^{-}e^{+i\omega_{2}t}+ E_{2}^{+}e^{-i\omega_{2}t}E_{1}^{-}e^{+i\omega_{1}t}\right>   \\ \\
 & = \frac{2}{\mu_{0}c}\left< E^{+}_{1}E^{-}_{1}+E^{+}_{2}E^{-}_{2}+ E_{1}^{+}E_{2}^{-}e^{i(\omega_{2}-\omega_{1})t}+E_{1}^{-}E_{2}^{+}e^{i(\omega_{1}-\omega_{2})t}   \right> 
\end{align}
$$

Assuming that $\omega_{2}-\omega_{1}$ is large enough, those time varying terms die. Thus,
$$
\begin{align}
I_{\text{ in }}  = \frac{2}{\mu_{0}c} \left< E_{1}^{+}E_{1}^{-} + E_{2}^{+}E_{2}^{-} \right> 
\end{align}
$$



We therefore have 
$$
\begin{align}
I_{\text{ out }}  & = \frac{1}{\mu_{0}c} (E_{1}^{+}E_{1}^{-}+E_{2}^{+}E_{2}^{-})\left( 1-\frac{E_{1}^{(+)}E_{1}^{(-)}\cos(\omega_{1}\tau)+E_{2}^{(+)}E_{2}^{(-)}\cos(\omega_{2}\tau)}{E_{1}^{2}+E_{2}^{2}} \right) \\
 & = \frac{1}{\mu_{0}c} \left( (E_{1}^{+}E_{1}^{-}+E_{2}^{+}E_{2}^{-})-E_{1}^{(+)}E_{1}^{(-)}\cos(\omega_{1}\tau)-E_{2}^{(+)}E_{2}^{(-)}\cos(\omega_{2}\tau) \right)
\end{align}
$$




![[Pasted image 20260207140438.png]]
We found previously that
$$
\begin{align}
I_{\text{ out }} & = \frac{1}{\mu_{0}c} \left( (E_{1}^{+}E_{1}^{-}+E_{2}^{+}E_{2}^{-})-E_{1}^{(+)}E_{1}^{(-)}\cos(\omega_{1}\tau)-E_{2}^{(+)}E_{2}^{(-)}\cos(\omega_{2}\tau) \right) \\
 & = \frac{1}{\mu_{0}c}(E_{1}^{2}+E_{2}^{2} - E_{1}^{2}\cos \omega_{1} \tau - E_{2}^{2} \cos \omega_{2} \tau)
\end{align}
$$

This is a constant $E^{2}_{1}+ E^{2}_{2}$ minus two cosine terms for each wave.
Combined, it gets the funkier but maybe nicer
$$
\begin{align}
I_{\text{ out }} = \frac{1}{\mu_{0}c}(E_{1}^{2}(1 - \cos \omega_{1}\tau) + E_{2}^{2}(1-\cos \omega_{2}\tau))
\end{align}
$$


![[Pasted image 20260207140447.png]]
$$
\begin{align}
I_{\text{ out }} = \frac{1}{2} I_{in}[1- Re g^{(1)}(t) ] 
\end{align}
$$
so 
$$
\begin{align}
\frac{I_{\text{ out }}}{I_{\text{ in }}} = \frac{1}{2}[1- Re(g^{1}(\tau))]
\end{align}
$$

This is

$$
\begin{align}
Re(g^{(1)}(\tau)) = \frac{E_{1}^{(+)}E_{1}^{(-)}\cos(\omega_{1}\tau)+E_{2}^{(+)}E_{2}^{(-)}\cos(\omega_{2}\tau)}{E_{1}^{2}+E_{2}^{2}}
\end{align}
$$


$$
\begin{align}
\frac{I_{\text{ out }} }{I_{\text{ in }} } = \frac{1}{2}\left[ 1- \frac{E_{1}^{2}\cos(\omega_{1}\tau)- E_{2}^{2}\cos(\omega_{2}\tau)}{E_{1}^{2}+E_{2}^{2}} \right]
\end{align}
$$

If we assume that $E_{1}^{2}=E_{2}^{2}$, then we get the nice trig identity.
$$
\begin{align}
\cos \theta + \cos \phi = 2\cos \frac{1}{2}(\theta+\phi)\cos \frac{1}{2}(\theta-\phi)
\end{align}
$$

We can relabel this in the context of our function as

$$
\begin{align}
2\cos \omega_{0}\tau \cos \Delta \omega \tau
\end{align}
$$
We get
$$
\begin{align}
\frac{I_{\text{ out }} }{I_{\text{ in }} } = 1- \frac{\cos \omega \tau \cos \Delta \omega \tau}{2 E_{0}^{2}}
\end{align}
$$

![[Pasted image 20260207140457.png]]

![[Pasted image 20260214213523.png]]




![[Pasted image 20260207140512.png]]
![[Pasted image 20260214211907.png]]
We know that
$$
\begin{align}
2\pi\omega \lambda & = c  \\
\omega_{1} &  = \frac{3e^{8} \text{ m }}{2\pi\cdot 589.6 \text{ s }\cdot \text{ nm }}  \\
 & = 8.098*10^{13} \\
\omega_{1} &  = \frac{3e^{8} \text{ m }}{2\pi\cdot 589 \text{ s }\cdot \text{ nm }}  \\
 &= 8.106*10^{13} 
\end{align}
$$


This gives us
$$
\begin{align}
\Delta \omega = -8.249 * 10^{10}  \\
\omega_{0} = 8.098*10^{13} 
\end{align}
$$



One may note that the modulation of the signal follows $\Delta\omega$
![[Pasted image 20260214214527.png]]
Thus the full period is crossed when
$$
\begin{align}
\Delta \omega \tau & =2\pi N\\
\tau  & =\frac{2(l_{1}-l_{2})}{c} \\
\Delta x  & = \frac{N\pi c}{\Delta \omega}
\end{align}
$$
Numerically, the first crossing is when
$$
\begin{align}
\Delta x = \frac{\pi c}{\Delta \omega}= 0.01142 \text{ m }
\end{align}
$$





![[Pasted image 20260207140527.png]]
![[Pasted image 20260214222033.png|300]]
We can calculate this.

We know that 
$$
\begin{align}
\Delta \omega =8.244 \times 10^{10}  \\
\omega_{0} = 8.097 \times 10^{13}
\end{align}
$$
the mass of sodium is $m=22.99$ grams per mol
This gives us 
$$
\begin{align}
\sigma_{w}^{2}  & = 1.792854611\times10^{-10}\\
\sigma_{w}  & =0.0000133915950597
\end{align}
$$
This gives us
$$
\begin{align}
\frac{\sigma_{\omega} }{\Delta \omega} \approx 0.00143
\end{align}
$$





![[Pasted image 20260207140536.png]]
![[Pasted image 20260214222033.png|300]]


$$
\begin{align}
1=\frac{1}{2} \frac{1}{\sqrt[]{ 2\pi \sigma_{\omega}^{2}  } }\int_{0}^{\infty} e^{\frac{-(\omega-\omega_{0})^{2}}{2 \sigma_{\omega}^{2} }}d\omega + \frac{1}{2}\frac{1}{\sqrt[]{ 2\pi \sigma_{\omega}^{2}  } }\int_{0}^{\infty} e^{\frac{-(\omega-\omega_{1})^{2}}{2 \sigma_{\omega}^{2} }}
\end{align}
$$
I calculated this to check that it was normalized (it was), then deleted it since I thought I did the wrong thing and started on the work below. Because we aren't asked to explicitly check, I figure it is fine to just leave the formula.
# old work
I am confused by this - the next step is calculating the coherence from the Doppler shifting intensity function, so I can't use the coherence function from before. But that means this is just copying from the slides. I started the derivation if we were using the $g^{(1)}$ that we calculated in problem 1 for two different equal intensity frequencies. 
$$
\begin{align}
Re(g^{(1)}(\tau)) = \frac{E_{1}^{(+)}E_{1}^{(-)}\cos(\omega_{1}\tau)+E_{2}^{(+)}E_{2}^{(-)}\cos(\omega_{2}\tau)}{E_{1}^{2}+E_{2}^{2}}
\end{align}
$$
If we have equal amplitudes, this is
$$
\begin{align}
Re(g^{(1)}(\tau))  & = \frac{E_{0}^{2}(\cos(\omega_{1}\tau)+\cos(\omega_{2}\tau))}{2E_{0}^{2}} \\
 & = \frac{1}{2} (\cos(\omega_{1}\tau)+\cos(\omega_{2}\tau))
\end{align}
$$



![[Pasted image 20260215105426.png|300]]
We therefore have
$$
\begin{align}
\frac{1}{\pi} \int_{0}^{\infty} \cos(\omega_{1}\tau)\cos(\omega \tau)+\cos(\omega_{2}\tau)\cos\omega \tau \,  \, \, d\tau
\end{align}
$$
We can rewrite this using trig identities
Lets use a dummy variable $x$, since this process will look the same for $\omega_{1}$ and $\omega_{2}$ in the overall integral.

$$
\begin{align} 
 & \frac{1}{\pi}\int_{0}^{\infty} \cos(x\tau)\cos(\omega \tau)d \tau \\
 & =\frac{1}{2\pi} \int_{0}^{\infty} \cos((x+\omega)\tau) + \cos((x-\omega)\tau)\, \, \, d\tau  \\

\end{align}
$$
This doesn't converge. What.



$$
\begin{align}
\frac{1}{\pi}\int_{0}^{\infty} 2\cos\left( \frac{\omega_{1}+\omega_{2}}{2} \right)\cos\left( \frac{\omega_{1}-\omega_{2}}{2} \right)\cos \omega \tau \, d\tau
\end{align}
$$


![[Pasted image 20260207140547.png]]
Using the formula 
$$
\begin{align}
g^{(1)}(\tau) = \int_{0}^{\infty} S(\omega)e^{-i\omega \tau}d\omega \\
\frac{1}{\sqrt[]{ 2\pi \sigma_{\omega}^{2}  } }\int_{0}^{\infty} e^{\frac{-(\omega-\omega_{0})^{2}}{2 \sigma_{\omega}^{2} }} e^{-i\omega \tau}d\omega 
\end{align}
$$

I will do this once, using $\omega_{0}$. This will be the exact same result as the second part of the gaussian, which will replace $\omega_{0}$ with $\omega_{1}$. 

Lets relabel $\omega-\omega_{0}$ as $x$. This is symmetric about 0, so we can make the integral easier by extending the bounds. Lets also relabel $a = \frac{1}{2 \sigma^{2}_{\omega}}$ 
$$
\begin{align}
 & \frac{1}{\sqrt[]{ 2\pi \sigma_{\omega}^{2}  } }\int_{-\infty}^{\infty} e^{-ax^{2}}e^{-i(x+\omega_{0}) \tau}dx \\
 & =\frac{1}{\sqrt[]{ 2\pi \sigma_{\omega}^{2}  } }\int_{-\infty}^{\infty} e^{-ax^{2}-i\tau x-i\omega_{0} \tau}dx  \\
\text{ let } b \equiv  i\tau\\
& =\frac{1}{\sqrt[]{ 2\pi \sigma_{\omega}^{2}  } }e^{-i\omega_{0} \tau}\int_{-\infty}^{\infty} e^{-(ax^{2}+b x)}dx
\end{align}
$$
Following the derivation of Appendex D of Townsend "A modern approach to quantum mechanics", this is in the same form as EQ D.5 with the result D.7
$$
\begin{align}
\int_{-\infty}^{\infty} dx e^{-ax^{2}+bx} = e^{\frac{b^{2}}{4a}} \sqrt[]{ \frac{\pi}{a} } 
\end{align}
$$
Our problem is now
$b^{2} = -\tau^{2}$. $4a = \frac{2}{\sigma^{2}_{\omega}}$
$$
\begin{align}
g^{(1)}(\tau)_{\omega_{0}}  & =\frac{1}{\sqrt[]{ 2 \pi \sigma^{2}_{w}  } }e^{-i\omega_{0}\tau} e^{\frac{-\tau^{2} \sigma^{2}_{\omega} }{2}}\sqrt[]{ 2\pi \sigma^{2}_{w}  } \\
 & = e^{-i\omega_{0}\tau}e^{- \frac{\tau^{2} \sigma^{2}_{\omega} }{2}} 
\end{align}
$$
We have to add the component from the other frequency of the doublet, so this becomes
$$
\begin{align}
g^{(1)}(\tau) & =\frac{1}{2} \frac{1}{\sqrt[]{ 2 \pi \sigma^{2}_{w}  } }e^{-i\omega_{0}\tau} e^{\frac{-\tau^{2} \sigma^{2}_{\omega} }{2}}\sqrt[]{ 2\pi \sigma^{2}_{w}  } \\
 & = \frac{1}{2}e^{- \frac{\tau^{2} \sigma^{2}_{\omega} }{2}} (e^{-i\omega_{0}\tau} + e^{-i\omega_{1}\tau}) 
\end{align}
$$



![[Pasted image 20260207140557.png]]
$$
\begin{align}
g^{(1)}(\tau) = \frac{1}{2} e^{-i\omega_{0}\tau}e^{- \frac{\tau^{2} \sigma^{2}_{\omega} }{2}} 
\end{align}
$$


Therefore, we have
$$
\begin{align}
\frac{1}{2}\int_{-\infty}^{\infty}\left|  \cos(-\omega_{0}\tau)e^{\frac{-\tau^{2} \sigma_{\omega} ^{2}}{2}} \right|^{2}  d\tau
\end{align}
$$
We can rewrite this and combine.
$$
\begin{align}
\cos(x) = \frac{e^{ix}+e^{-ix}}{2}
\end{align}
$$
This gets
$$
\begin{align}
  & \, \, \, \, \, \, \, \, \frac{1}{4}\int_{-\infty}^{\infty} \left|e^{i\omega_{0}\tau-\tau^{2} \sigma^{2}_{\omega} } + e^{-i\omega_{0} \tau - \tau^{2} \sigma^{2}_{\omega} }   \right| ^{2} d \tau \\
 & = \frac{1}{4}\int_{-\infty}^{\infty}  2e^{-2\tau^{2} \sigma^{2}_{\omega} } + e^{2i\omega_{0}\tau - 2\tau^{2} \sigma^{2}_{\omega} }+e^{-2i\omega_{0}\tau - 2\tau^{2} \sigma^{2}_{\omega} } \, \, d \tau \\
\end{align}
$$


Lets break this into three Gaussians
### Gaussian 1
$$
\begin{align}
2e^{-2\tau^{2} \sigma^{2}_{\omega} }
\end{align}
$$
These have well explored solutions.
$$
\begin{align}
\int_{-\infty}^{\infty} e^{-a x^{2}}= \sqrt[]{ \frac{\pi}{a} } 
\end{align}
$$
This whole expression evaluates to
$$
\begin{align}
\frac{1}{2}\sqrt[]{ \frac{\pi}{2\sigma^{2}_{\omega} } } 
\end{align}
$$
### Gaussian 2
$$
\begin{align}
e^{2i\omega_{0}\tau - 2\tau^{2} \sigma^{2}_{\omega} }\\
\int_{-\infty}^{\infty} e^{-ax^{2}+bx} = e^{\frac{b^{2}}{4a}}\sqrt[]{ \frac{\pi}{a } } 
\end{align}
$$
Here, $b^{2}=-4\omega_{0}^{2}$
and $\frac{1}{4a}=\frac{1}{8\sigma^{2}_{\omega}}$
This whole expression gives us
$$
\begin{align}
\frac{1}{4} e^{\frac{-\omega_{0}^{2}}{2\sigma_{\omega}^{2}} }\sqrt[]{ \frac{\pi}{2\sigma^{2}_{\omega} } } 
\end{align}
$$

### Gaussian 3
$$
\begin{align}
e^{-2i\omega_{0}\tau - 2\tau^{2} \sigma^{2}_{\omega} } \, \, d \tau
\end{align}
$$
$b^{2} = -4i\omega_{0}^{2}$. 
$\frac{1}{4a}= \frac{1}{8\sigma^{2}_{\omega}}$
We have the same process as for Gaussian 2. This gets the same exact result as Gaussian 2. 

### Continuing the result
We now have for $\omega_{0}$:
$$
\begin{align}
\tau_{\text{ coh }} = \frac{1}{2}\sqrt[]{ \frac{\pi}{2\sigma^{2}_{\omega} } } \left( 1+e^{\frac{-\omega_{0}^{2}}{2\sigma_{\omega}^{2}} } \right) + \frac{1}{2}\sqrt[]{ \frac{\pi}{2\sigma^{2}_{\omega} } } \left( 1+e^{\frac{-\omega_{1}^{2}}{2\sigma_{\omega}^{2}} } \right)
\end{align}
$$
And the coherence length
$$
\begin{align}
\mathscr{l}_{\text{ coh }} = \frac{c}{2}\sqrt[]{ \frac{\pi}{2\sigma^{2}_{\omega} } } \left( 1+e^{\frac{-\omega_{0}^{2}}{2\sigma_{\omega}^{2}} } \right) + \frac{c}{2}\sqrt[]{ \frac{\pi}{2\sigma^{2}_{\omega} } } \left( 1+e^{\frac{-\omega_{1}^{2}}{2\sigma_{\omega}^{2}} } \right)
\end{align}
$$

This gives 
$$
\begin{align}
\tau_{\text{ coh }}  & = 9.3*10^{-6} \text{ seconds } \\
\lambda_{\text{ coh }} &  = 2808.07 \text{ m }
\end{align}
$$







# old work
$$
\begin{align}
 & = \frac{1}{2} \int_{-\infty}^{\infty} 2e^{2\tau^{2} \sigma_{\omega} ^{2}} + e^{(2\tau^{2} \sigma^{2}_{\omega} )}(e^{2i\omega_{0}\tau}+e^{-ti\omega_{0}\tau}) d \tau \\
& = \frac{1}{2} \int_{-\infty}^{\infty} 2e^{2\tau^{2} \sigma_{\omega} ^{2}} +2 e^{(2\tau^{2} \sigma^{2}_{\omega} )}\cos(2\omega_{0}\tau) \, d \tau \\
& = \frac{1}{2} \int_{-\infty}^{\infty} 2e^{2\tau^{2} \sigma_{\omega} ^{2}} (1+\cos(2\omega_{0}\tau)) \, d \tau
\end{align}
$$


![[Pasted image 20260207140609.png]]

$$
\begin{align}
g^{(1)}(\tau) = \frac{1}{2} e^{-i\omega_{0}\tau}e^{- \frac{\tau^{2} \sigma^{2}_{\omega} }{2}} 
\end{align}
$$
We know that

$$
\begin{align}
I_{\text{ out }} = \frac{1}{2} I_{in}[1- Re g^{(1)}(t) ] 
\end{align}
$$

This gives the relative intensity
$$
\begin{align}
\frac{I_{\text{ out }}}{I_{\text{ in }} }= \frac{1}{2}\left( 1- \frac{1}{2}\cos(\omega_{0}\tau)e^{\frac{-\tau^{2}\sigma^{2}_{\omega} }{2}} \right) 
\end{align}
$$

![[Pasted image 20260207140624.png]]

However, the bands are Doppler broadened - but we really care about the distance between the centers of the two Gaussians that describe the light. That is the distance that one must travel to see light patterns from alignment of one frequency and not the other. 

If we thought that the beams were perfect (no broadening), then we would see peaks of them offset by a length corresponding the difference in the frequencies. The seperation in frequency between them is 
$$
\begin{align}
2 \Delta \omega = 2 * 8.244 \times 10^{10} 
\end{align}
$$

We can convert this to length as
$$
\begin{align} \\
2\pi\omega \lambda & = c \\
\delta \mathscr{l}_{\text{ width }}   & = \frac{c}{2\pi \omega} \\
\delta \mathscr{l}_{\text{ width }} & = \frac{c}{4\pi \Delta \omega }  \\
 & = 0.000289 m
\end{align}
$$







