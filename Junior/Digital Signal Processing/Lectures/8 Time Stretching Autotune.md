Goal: Change playback speed without changing the frequency content. 

This is the same as changing pitch without changing the tempo. Same math. 

If we change the sampling rate:
$$
\begin{align}
\mathscr{F} \left\{ x(t) \right\}= \int_{-\infty}^{\infty} x(t)e^{-j\omega t}dt \\
\mathscr{F} \left\{ x(at) \right\}= \int_{-\infty}^{\infty} x(at)e^{-j\omega t}dt
\end{align}
$$
We can u-sub with $u=at, du=a\,dt$ to get
$$
\begin{align}
\mathscr{F} \left\{ x(at) \right\}= \frac{1}{a} \int_{-\infty}^{\infty} x(u)e^{-j \frac{\omega}{a}u}du
\end{align}
$$

This is just a dummy variable, so it really just looks like the Fourier transform but mapping frequencies from $\omega$ to $\frac{\omega}{a}$. This gives
$$
\begin{align}
\mathscr{F} (x(at))= \frac{1}{a} X\left( j \frac{\omega}{a} \right)
\end{align}
$$
When time is stretched by a factor $a$, each frequency $\omega$ gets mapped to $\frac{\omega}{a}$. 

We have three possible approaches:

## Overlap-Add (OLA) (bad approach)
1) We take a signal, DON'T do any Fourier. We break up the actual signal with a hopsize. We grab fixed analysis frames at each hop distance, with a length $n$.
2) Synthesis frames - we put the frames together with a different hop size. If the hop if smaller, than we go through the data far faster. The analysis hop size is different from the synthesis frame. We have a stretching factor $\alpha= \frac{H_{s}}{H_{a}}$. Usually $H_{s}$ is fixed, so we figure out what $H_{a}$ to use by rearranging.
The new frame mapping is
$$
\begin{align}
\underbrace{ y_{m} }_{ \text{ synthesis } }[n] = \frac{\overbrace{w[n]}^{\text{ window }} \cdot \overbrace{x_{m}[n]}^{\text{ analysis }}  }{\sum_{k}^{} w[n-kH_{s} ]} 
\end{align}
$$
The window must have a constant add (COLA condition from before). 
3) Signal reconstruction

$$
\begin{align}
\underbrace{ y[n] }_{ \text{ time streched } }= \sum_{k}^{} y_{m}[n-kH_{s} ]
\end{align}
$$

### Pros and Cons
#### Cons
Can't preserve periodic structures - we are adding the music signal to itself, so if things don't line up then it completely changes the structures.

Transient doubling - If there are sharp transient signals that exist entirely with small portions of a window, then we might copy it multiple times when we make multiple frames. We can mitigate it with small N. 
#### Pros
Preserves Timbre really well. This is good for percussive signals but not for pitches. 


## Instantaneous Frequency Estimation


## Phase Vocoder
