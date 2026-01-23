Day to day variation causes error: I.e. day to day temperature fluctuations might change the power available for a laser? (check this?).


One standard deviation is $\frac{1}{\sqrt[]{ e }}$ away - about 63%.


Imagine taking 5 data points to get $\bar{y}$. If a million people did 5 trials, the $\bar{y}$ has its own distribution.
As $N\to \infty$, the $\bar{y}$ distribution has a mean $\mu$ (true mean) and standard deviation $\frac{\sigma}{\sqrt[]{ N }}$, which is the Standard Error of Measurement. 


## Goal of lecture
Given $N$ trials $\left\{ y_{1},y_{2},\dots,y_{n} \right\}$ drawn independently, each according to probability distribution $P(y)$ with mean $\mu$ and variance $\sigma^{2}$ unknown to us, estimate $\mu$ and attach an uncertainty to our estimate of $\mu$.

Sample mean is an unbiased estimate of $\mu$
$$
\begin{align}
\bar{y} = \frac{1}{N} \sum_{n=1}^{N} y_{n} 
\end{align}
$$
The sample variance is an unbiased estimate of the variance $\sigma^{2}$
$$
\begin{align}
s^{2} = \frac{1}{N-1} \sum_{n=0}^{N} (y_{n}-\bar{y})^{2}
\end{align}
$$

And the standard error of the mean gives the uncertainty of $\bar{y}$ as an estimate of $\mu$.  This is the distribution that the $\bar{y}$ s follow, with a standard deviation well approximated by
$s_{\bar{y}}= \frac{s}{\sqrt[]{ N }}$.

SEM is the size of error bars for each data points. 

### Mean and variances 
$$
\begin{align} 
 \text{ total probability}  & \text{ is 1 (normalization) }  \\
 & \int_{-\infty}^{\infty} P(y)dy = 1 \\
\text{ mean: }  & \\
 & \left< y \right>  \equiv \int_{-\infty}^{\infty} y P(y) dy = \mu \\
\text{ variance: } &  \\
 & \left< (y-\mu)^{2} \right>  \equiv  \int_{-\infty}^{\infty} (y-\mu)^{2}P(y)dy = \sigma^{2} \\
\text{ Standard Dev }: \\
 & \sqrt[]{ \sigma^{2} } 
\end{align}
$$

For a normal distribution,
$$
\begin{align}
\int_{\mu-\sigma}^{\mu+\sigma} P(y)dy \approx 0.68 
\end{align}
$$
for $2\sigma$ it is 0.95, and $3\sigma$ is 0.997.



>[!abstract]+ Warmup
>y is drawn from $P(y)$, z is drawn from $P(z)$, with respective means and variance. 
>They are drawn independently, so $P(y,z)=P(y)P(z)$.
>If we have a function $f(y,z)$, we make a linear approximation
> $f(y,z)\approx f(\mu_{y},\mu_{z})+ \frac{ \partial f }{ \partial y }\bigg|_{\mu_{y},\mu_{z}}^{}(y-\mu_{y}) + \frac{ \partial f }{ \partial z }\bigg|_{\mu_{y},\mu_{z}}^{}(z-\mu_{z})$
> We can propagate error. 
> $$
> \underbrace{ \left< f(\mu_{y},\mu_{z}) \right> }_{ f(\mu_{y},\mu_{z}) } +\left<  \frac{ \partial f }{ \partial y }\bigg|_{\mu_{y},\mu_{z}}^{}(y-\mu_{y}) \right>   + \left< \frac{ \partial f }{ \partial z }\bigg|_{\mu_{y},\mu_{z}}^{}(z-\mu_{z}) \right>  
> $$
> 
> $$
> \left< [f(y,z)- f(\mu_{y}, \mu_{z}) ]^{2}  \right>  \\
> = \left< \left[ \frac{ \partial f }{ \partial y } \bigg|_{\mu_{y},\mu_{z} }^{}(y-\mu_{y} ) + \frac{ \partial f }{ \partial z } \bigg|_{\mu_{y} , \mu_{z} }^{}     \right]^{2} \right> \\
> \text{ which we can foil into three terms }
> = \left< \underbrace{ \left( \frac{ \partial f }{ \partial y } \bigg|_{\mu_{y} ,\mu_{z} }^{}   \right)^{2} }_{ \text{ constant } }\underbrace{ (y-\mu_{y} )^{2} }_{ \text{ variance for y } } \right>  + \left< \left( \frac{ \partial f }{ \partial z } \bigg|_{\mu_{y} , \mu_{z} }^{}  \right)^{2} \underbrace{ (z-\mu_{z} )^{2} }_{ \sigma_{z} ^{2} } \right> + 2 \left< \frac{ d f}{d y } \bigg|_{\mu_{y} ,\mu_{z} }^{} \frac{ d f}{d z } \bigg|_{\mu_{y} ,\mu_{z} }^{} (y-\mu_{y} )(z-\mu_{z} )   \right>   
> $$
> We can calculate this last term as
> $$
> \left< (y-\mu_{y} )(z-\mu_{z} ) \right>  = \iint (y-\mu_{y} )(z-\mu_{z} )P(y,z)dydz
> $$
> but because they are independent, $P(y,z)=P(y)P(z)$ so we have this last term as $\left<  y-\mu _{y}\right>\left< z-\mu_{z} \right> = 0\cdot 0$
> Therefore, we have found that
> $$
> \left< [f(y,z)-f(\mu_{y} ,\mu_{z} )]^{2} \right>  =  \left( \frac{ \partial f }{ \partial y } \bigg|_{\mu_{y} ,\mu_{z} }^{}   \right)^{2} \sigma_{y} ^{2} + \left( \frac{ \partial f }{ \partial z } \bigg|_{\mu_{y} ,\mu_{z}  }^{}   \right)\sigma_{z} ^{2}  \\
> \omega^{2}_{f} \approx \left( \frac{ \partial f }{ \partial y }  \right)^{2}\sigma_{y} ^{2} + \left( \frac{ \partial f }{ \partial z }  \right)^{2} \sigma^{2}_{z} \\
> $$







Lets prove things. That for N independent trials, 
$\bar{y}= \frac{1}{N}(y_{1}+y_{2}+\dots+y_{n})$
$$
\begin{align}
\left< \bar{y} \right>=\frac{1}{N}\sum \left< y_{n} \right> \\
= \frac{1}{N} N\mu = \mu  
\end{align}
$$

What is the variance of $\bar{y}?$

$$
\begin{align}
\bar{y} = \frac{1}{N} (y_{1}+y_{2}+\dots+y_{n})  & = \frac{1}{N}\sum_{n=1}^{N} y_{n} \\
\left< (y_{n}-\mu)^{2} \right>   & =\sigma^{2} \\
\left< (\bar{y}-\mu^{2}) \right>  &  = \left< \left( \frac{1}{N} \sum_{n=1}^{N} y_{n} \right)- \frac{N\mu}{N} \right>   \\
 & = \left< \frac{1}{N^{2}}\left( \sum_{n=1}^{N} (y_{n}-\mu) \right)^{2} \right>  
\end{align}
$$
This has $N$ terms that look like $\left<  (y_{n}-\mu)^{2}\right> =\sigma^{2}$, and a bunch of terms like $\left< (y_n-\mu)(y_{m}-\mu) \right> = 0$
So, we have 
$$
\begin{align}
\left< (\bar{y}-\mu)^{2} \right>  = \frac{1}{N^{2}}N \sigma^{2} = \frac{\sigma^{2}}{N}
\end{align}
$$
If we let a million people do a 5 trials experiment ($N=5$), then we see that the expectation value of the variance decreases by $N$ - which is what leads to SEM $=\frac{\sigma}{\sqrt[]{ N }}$.

However, if we don't know what $\sigma$ is in an experiment (which is most of the time), we need to estimate $\sigma$.

We claim that the sample variance is an unbiased estimate of variance.
$\left< s^{2} \right> = \sigma^{2}$

$$
\begin{align}
\left< s^{2} \right>  = \left< \frac{1}{N-1} \sum_{n=1}^{N}(y_{n}-\bar{y})^{2}  \right>   \\
= \frac{1}{N-1} \sum_{n=1}^{N} \underbrace{ \left< (y_{n}-\bar{y})^{2} \right>    }_{ \text{ smaller than }\sigma^{2} \text{ because }y_{n} \text{ helped d} }
\end{align}
$$
Lets do this.
$$
\begin{align}
\left< (y_{n}- \bar{y})^{2} \right>  &  = \left< [(y_{n}-\mu)-(\bar{y}-\mu)]^{2} \right>   \\
 & =\left< (y_{n}-\mu)^{2} \right>  + \left< \bar{y}-\mu \right>  ^{2} - 2 \left< (y_{\bar{n}} -\mu)(\bar{y}-\mu) \right>   \\
 & = \sigma^{2} + \frac{\sigma^{2}}{N} - 2 \xi \\
\text{ where } \\
 & \xi = \left< (y_{n}-\mu)(\bar{y}-\mu) \right>  = \underbrace{ \left< (y_{n}-\mu) \left( \frac{1}{N} \sum_{i=1}^{N} (y_{i} -\mu) \right)\right>   }_{ \frac{1}{N}\times \text{ 1 term } \left< (y_{n}-\mu)^{2} \right> \text{ and a bunch of } 0      }
\end{align}
$$
$$
\begin{align}
\left< (y_{n}-\bar{y})^{2} \right>  = \sigma^{2} + \frac{\sigma^{2}}{N} - 2 \underbrace{ \xi }_{ \frac{\sigma^{2}}{N} }  \\
= \sigma^{2} \left(  1- \frac{1}{N} \right)= \sigma^{2}\left( \frac{N-1}{N} \right)
\end{align}
$$

so our best estimate of SEM is
$\mu=\bar{y} + \frac{s}{\sqrt[]{ N }}$

$$
\begin{align}
s = \sqrt[]{ \frac{1}{N-1}\sum_{n=1}^{N} (y_{n}-\bar{y})^{2} } 
\end{align}
$$






