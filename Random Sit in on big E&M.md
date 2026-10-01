$$
\begin{align}
\hat{R} = \sqrt{\dfrac{\hat{V}}{W}},
\qquad
\hat{V} = \frac{N-1}{N}\,W + \frac{1}{N}\,B \\
\end{align}
$$
$$
\begin{align}
W = \frac{1}{M}\sum_{c=1}^{M} s_c^{2},
\qquad \\
s_c^{2} = \frac{1}{N-1}\sum_{n=1}^{N}\bigl(\theta_{c,n}-\bar{\theta}_c\bigr)^{2},
\qquad\\
B = \frac{N}{M-1}\sum_{c=1}^{M}\bigl(\bar{\theta}_c-\bar{\theta}\bigr)^{2},
\end{align}
$$



where $\theta{c,n}$ is draw $n$ of chain $c$, $\bar{\theta}c$ the chain mean, $\bar{\theta}$ the pooled mean, $M$ chains of length $N$ (post-burn; for split-$\hat{R}$ each chain is halved so $M\to 2M$, $N\to N/2$).

s_c^2 is the variance of a single chain
W is the average variance of chains
B is the variance of the average draw across chains


$$
\boxed{\;\hat R=\sqrt{\dfrac{N-1}{N}+\dfrac{M}{M-1}\cdot\dfrac{\sum_c(\bar\theta_c-\bar\theta)^2}{\sum_c s_c^2}}\;}
$$

$$
\frac{M}{M-1}\cdot\frac{\sum_c(\bar\theta_c-\bar\theta)^2}{\sum_c s_c^2}=\frac{\widehat{\operatorname{Var}}(\bar\theta_c)}{W},\qquad \widehat{\operatorname{Var}}(\bar\theta_c)=\frac{1}{M-1}\sum_c(\bar\theta_c-\bar\theta)^2
$$


i.e. **(variance of the chain means) ÷ (mean within-chain variance)** — so

$$\hat R=\sqrt{\frac{N-1}{N}+\frac{\widehat{\operatorname{Var}}(\bar\theta_c)}{W}}$$




- **$\dfrac{N-1}{N}$** — the *long-run floor*. It's the weight on the within-chain variance $W$ inside $\hat V$. With a finite chain of length $N$, $W$ slightly under-counts the true marginal variance, so this factor sits just below 1 and $\to 1$ as $N\to\infty$. It's the value $\hat R^2$ collapses to once the chains stop disagreeing.

- **$\dfrac{M}{M-1}$** — the *finite-number-of-chains (Bessel) correction*. You're estimating the spread of the chain means from only $M$ chains, so the unbiased sample variance divides by $M-1$. It $\to 1$ as $M\to\infty$; with $M=24$ it's $\approx 1.04$ — a small inflation.

- **$\dfrac{\sum_c(\bar\theta_c-\bar\theta)^2}{\sum_c s_c^2}=\dfrac{\widehat{\operatorname{Var}}(\bar\theta_c)}{W}$** — the actual diagnostic: **between-chain scatter measured in units of within-chain scatter**. It asks "are the chains' centers sitting far apart *relative to how wide each chain is*?" If the chains overlap (well-mixed), the chain means agree, numerator $\to 0$, and $\hat R\to 1$. If chains are trapped in different modes (our capped minutes), the means are far apart relative to each chain's width, this term blows up, and $\hat R\gg 1$.

So $\hat R$ is fundamentally **(total variance if you trust the spread of the chains) / (variance within a single chain)** — a ratio that equals 1 only when looking at all chains together tells you nothing more than looking at one.


$$
\begin{align}
\hat{R} = \sqrt{\frac{N-1}{N} + \frac{B}{W}} \\
\end{align}
$$
$$
\begin{align}
\hat{R} = \sqrt[]{ \frac{N-1}{n} + \frac{M-1}{M} \sum_{c=1}^{M}  \frac{(\bar{\theta}_{c} -\bar{\theta})^{2}}{s_{c}^{2} } } 
\end{align}
$$

