Measurements depend on measurement resolution, and can have systematic or random error incorporated. Usually, measurement error is $\pm$ the smallest measurement$/\sqrt{ 12 }$. This is because flat probability distributions with a width $x$ has a standard deviation $\sigma=\frac{x}{\sqrt{ 12 }}$.

Accuracy describes systematic error, i.e. how close measurements are to the true value. If there is a constant offset from measuring devices etc, this is systematic.

Precision describes random error, its the spread of data points. 

The Standard error of measurement (SEM) is 
$$
\begin{align}
\frac{\sigma_{r}}{\sqrt{ n }} = \sqrt{ \left( \frac{\sum_{i=1}^{N}(x_{i}-\bar{x})^{2}}{N(N-1)} \right) }
\end{align}
$$
This represents the uncertainty of the average. 

We can calculate the error in our output from a function by the error in the input.
$$
\begin{align}
\delta f \approx \left| \frac{df}{dx} \right| \delta x \\ 
\end{align}
$$
Lets take a circle. 
$$
\begin{align}
A=\pi r^{2}
\end{align}
$$
We can find error in the output by error in the input r.
$$
\begin{align}
\delta A &  \approx \left| \frac{dA}{dr} \right| \delta r \\
 & = 2\pi r \times    \delta r
\end{align}
$$
For dropping the ruler, our function is
$T = \sqrt{ \frac{2d}{g} }$
We can propagate it. 
$\frac{dT}{dd}=\frac{1}{2} (\frac{2d}{g}) ^{-1/2}$

so the error is $\frac{\delta d}{\sqrt{ 2\bar{d}g }}$.


With multiple errors, we propigate SEM as
$$
\begin{align}
\delta \lambda=\sqrt{\left( \frac{ \partial \lambda }{ \partial \lambda_{eff}  } \nabla\lambda_{eff} \right)^{2}+\left( \frac{ \partial \lambda }{ \partial n } \nabla n \right) ^{2}  }
\end{align}
$$

$$
\begin{align}
\text{ s }\left( \frac{n\pi}{1+n\pi} \right)
\end{align}
$$