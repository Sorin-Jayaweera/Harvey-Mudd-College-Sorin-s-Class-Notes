## STFT
We want both time and frequency information
$$
\begin{align}
S[\underbrace{ m }_{ \text{ frame idx } },\underbrace{ k }_{ \text{ freq idx } }] = \underbrace{ \sum_{n=0}^{N-1} }_{ \text{ window size } } x[m\cdot \underbrace{ \Delta }_{ \text{ hop size } } + n] \underbrace{ \omega[n] }_{ \text{ window function } } \underbrace{ e^{-j \frac{2\pi}{N}nk}U }_{ Fourier }
\end{align}
$$
![[Pasted image 20260127102232.png|300]]


Window size: Always a power of 2
Window type: Hanning, Hamming, etc. Gets rid of edge artifacts. We want frames to overlap because we don't want to ignore the data at the beginning and end of the window.  

Hop size: Distance between consecutive frames.  We can convert from frame index to time with $\Delta_{\text{ seconds }}= \frac{\Delta_{\text{ samples }}}{f_{s}}$

Sampling rate: $f_{s}$
If we want to go from index to time,
Frame $m\to m \cdot \frac{\Delta_{\text{ samples }}}{f_{s} }$
Frequency $k\to  \frac{k}{N}f_{s} \text{ Hz }$ when $K \leq \frac{N}{2}$.

compute STFT and plot the spectrogram
``` python
await micropip.install("scipy")
from scipy.signal import stft
x = signal
f,t, Sxx = stft(x,fs,nperseg=512)
plt.imshow(np.abs(Sxx),origin='lower')
plt.show()
```


### Exercise:

We have a 16 kHz signal with 3 pure tones of frequency 262, 292, 330, each lasting 1 second. The frame width is $N=512$. $\Delta=10ms$
Draw the STFT.

The delta $\Delta=160$ samples. We have $512$ rows (or $\frac{512}{2}$ if we only have the real frequencies). For three seconds long, we have 
$\frac{48000 \text{ samples }}{160 \text{ samples in a window }}\approx300 \text{ frames }$

Lets find the $k$ values. 
$$
\begin{align}
f = 262 Hz = k f_{s} \frac{1}{N}  \\
\implies k \approx 8.4 
\end{align}
$$
The DFT has complex conjugate symmetry, so we also have $N-k_{1}=503.6$.

![[Pasted image 20260129102852.png|300]]

## Inverse STFT

If there is a constant overlap add between each frame, then yes. This means that adding each window leads to a constant value. 

A Hann window with $\Delta = \frac{N}{2}$ satisfies this. The window and the hop size matters. The sum of all the windows overlapping has to be constant.
![[Pasted image 20260129103638.png|300]]


There is a useful function called scipy.signal.check_COLA to see if a window satisfies the condition. 

![[Pasted image 20260129103750.png|300]]









