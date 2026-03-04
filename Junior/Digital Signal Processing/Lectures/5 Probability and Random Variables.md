Math for me to easily reference
$\rho_{xy} = \frac{\sigma_{xy}}{\sigma_{x}\sigma_{y}}$
$\sigma_{xy}= E[(x-E[x])(Y-E[Y])]$
$\sigma_{x}^{2}= E[x^{2}]-E[x]^{2}$
$$
\begin{align}
\sigma_{xy}  & = E[XY]-E[X]E[Y]  
\end{align}
$$

This is an introduction, we'll take this to hidden Markov models etc. 

Any recording of data is not going to be deterministic, there will be noise and uncertainty etc. 

We have a sample space, $S:\text{ the set of all possible outcomes }$.
Inside there are sample points, which are single outcomes. There is a set of possible unique outcomes (even numbers of a dice roll, under three, or whatever) that we call an "event".


Conditional probability:
$P(A|B)$ is the probability of getting $A$ given $B$. 
$$
\begin{align}
P(A|B) &  = \frac{P(A \cap B)}{P(B)} \\
P(A \cap B) &  = P(A)P(B|A) \\
P(A|B) &  = \frac{P(A)P(B|A)}{P(B)} & \text{ (bayes rule) }
\end{align}
$$

Independence:
$$
\begin{align}
P(A|B) = P(A) \\
P(A\cap B) = P(A)P(B)
\end{align}
$$


Lets consider rolling two dice. 
$$
\begin{align}
A  & = \left\{ \text{ sum eveb } \right\} \\
B  & = \left\{ \text{ sum }\leq 6 \right\} \\
C  & = \left\{ \text{ 1 }^{st} \text{ roll is 1 } \right\}
\end{align}
$$
Are $A$ and $B$ independent? $A$ and $C$?
Roll 1 $\to$, Roll 2 $\downarrow$  

|     | 1   | 2   | 3   | 4   | 5   | 6   |
| --- | --- | --- | --- | --- | --- | --- |
| 1   | 2   | 3   | 4   | 5   | 6   | 7   |
| 2   | 3   | 4   | 5   | 6   | 7   | 8   |
| 3   | 4   | 5   | 6   | 7   | 8   | 9   |
| 4   | 5   | 6   | 7   | 8   | 9   | 10  |
| 5   | 6   | 7   | 8   | 9   | 10  | 11  |
| 6   | 7   | 8   | 9   | 10  | 11  | 12  |

$$
\begin{align}
P(A|B)  & = \frac{P(A,B)}{B}  & = \frac{3}{5} \\
P(A|C)  & = \frac{P(A,C)}{P(C)}  & =\frac{1}{2} 
\end{align}
$$


## Random Variables
We assign a number to an outcome as a number, and ask the probability that the number $X$ is equal to some value. We have probability mass distributions, and cumulative probability distributions. 



## Probability functions
### Probability mass function PMF
This is for discrete functions

$$
\begin{align}
P_{X}(x)   & = P(X=x) \\
\sum_{i}^{}  & P_{X} (x) =1  \\
0 \leq  & P_{X}   (x)  \leq 1 
\end{align}
$$

### Probability density function PDF
This is for continuous functions
 Gaussians are common PDFs.
 The actual value of the PDF is not a probability - it is a probability density. To get a probability, we calculate the area within a range of the curve.
$$
\begin{align}
f_{X}(x) \\
p(a_{1}<X<a_{2} ) &  = \int_{a_{1}}^{a_{2}} f_{X}(x)dx \\
\int_{-\infty}^{\infty}  f_{X}(x)dx & =1  
\end{align}
$$


## Common Distributions
For all of these we assume independence. 
### Discrete

#### Bernoulli distribution: 
a weighted coin flip
$$
\begin{align}
P(X=1)=p \\
P(X=0)=1-p \\
\end{align}
$$
#### Geometric distribution
$$
\begin{align}
P(X=k) = (1-p)^{k-1}p \\ 
k = 1,2,3,4,5
\end{align}
$$
How many times do I have to try something to get a success?

#### Binomial distribution
$$
\begin{align}
P(X=k) = \binom{n}{k} p^{k}(1-p)^{n-k} \\
\text{ for } k = 0,1,2,\dots n 
\end{align}
$$

If i have N trials and K successes, what is the probability of k successes and N-K failures? What is the probability of exactly 2 defective, or 4, etc? 

### Continuous

#### Uniform Distribution
$$
\begin{align}
f_{X}(x;a,b) = \begin{cases}
\frac{1}{b-a}, a \leq x\leq b \\
0 , \text{ else }
\end{cases}
\end{align}
$$

#### Exponential distribution
this is used to model the lifetime of a product.
If a product fails, it'll fail soon - if it lasts a while, it'll last a while.
$$
\begin{align}
f_{X}(x;\lambda) = \begin{cases}
\lambda e^{-\lambda x}, x \geq  0 \\
0, x < 0
\end{cases} 
\end{align}
$$

#### Gaussian Distribution
$$
\begin{align}
f_{X}(x,\mu,\sigma^{2}) = \frac{1}{\sqrt[]{ 2\pi\sigma^{2} } } e^{- \frac{1}{2 \sigma^{2}}(x-\mu)^{2}} 
\end{align}
$$

## Variables
We mainly describe variables with PMF and PDF. 
However, we also have a cumulative density function (which works for discrete or continuous variables)

$$
\begin{align}
F_{x}  & = P(x \leq x) \\
F_{X} (x) &  \leq  0  \\
F_{X}(\infty) & =1 \\
F_{X}(-\infty) & =0 \\
F_{X}(x)  & \text{ is non decreasing }   
\end{align}
$$

This is just the integral (or sum) of the PDF/PMF.

For the $PDF$, this is
$$
\begin{align}
F_{X}(x) = \int_{-\infty}^{x} f_{X}(x)   \\
\frac{ d F_{X}(x) }{d x } = f_{X} (x)
\end{align}
$$




We have joint pmfs and pdfs, where we make (lollipops for pmf) vs plane (pdf) of probability. This can go up to $n$ dimensions


If we want to know
$$
\begin{align}
P_{x}(x_{i} ) = \sum_{j}^{} P_{X}(x_{i},y_{j}  )  
\end{align}
$$


## Independence
$$
\begin{align}
P_{X,Y}(x,y) = P_{X}(x)P_{y}(y) \forall x,y\\
F_{X,Y}(x,y) = F_{X}(x)F_{y}(y) \forall x,y  \\ \\
p_{X,Y}(x,y) = p_{X}(x)p_{y}(y) \forall x,y\\
f_{X,Y}(x,y) = f_{X}(x)f_{y}(y) \forall x,y  \\ 
\end{align}
$$


## Stats
$$
\begin{align}
\text{ mean: } \\
\left< x \right>  & = \int_{-\infty}^{\infty} x f(x) dx \\
\text{ variance } \\
\sigma^{2} &  = \left< x ^{2}\right> - \left< x \right> ^{2} \\
\left< x^{2} \right>  & = \int_{-\infty}^{\infty} x^{2} f(x)dx  \\
\end{align}
$$
We can also look at the covariance of $X$ and $Y$. 

$$
\begin{align}
\sigma_{xy}  & = \left< (X-\left< X \right>) (Y-\left< Y \right> ) \\
 \right>  \\
 & = \left< XY \right> - \left< X \right> \left< Y \right> 
\end{align}
$$

The correlation coefficient,
$$
\begin{align}
\rho_{xy} = \frac{\sigma_{xy} }{\sigma_{x} \sigma_{y} }
\end{align}
$$
if $\sigma_{xy}=0$, then $X$ and $Y$ are uncorrelated.
Uncorrelated does not mean independent. 

## Multivariate Gaussian
$$
\begin{align}
\text{ cov }[x] = \Sigma  = E[\underbrace{ (x-\mu) }_{ \mathbb{R}^{^{D\times 1}}  }\underbrace{ (x-\mu)^{T} }_{ \mathbb{R}^{1\times D}  }] \in \mathbb{R}^{D\times D} 
\end{align}
$$
$$
\begin{align}
f_{X}(x) = \frac{1}{\sqrt[]{ (2\pi)^{D} \left| \Sigma \right|  } } e^{- \frac{1}{2}(x-\mu)^{T}\Sigma ^{-1}(x-\mu)}
\end{align}
$$
The diagonals of the covariance matrix
$$
\begin{align}
\begin{bmatrix}
 & x_{1} & x_{2} & \dots & x_{n} \\
x_{1}  & \sigma_{x _{1}x_{1} }  & \sigma_{x _{2}x_{1} }  & \dots & \sigma_{x _{n}x_{1} }   \\
x_{2}  & \sigma_{x _{i}x_{j} } \\
\vdots \\
x_{n}
\end{bmatrix}
\end{align}
$$
The diagonal elements are variance with oneself. 

## Maximum Likelihood Estimation

Given several possible models, which is the most likely?
I.e. transmitting bits in radio, is it most likely that the message is a 1 or a 0?

We pick the model with the maximum probability of observing the data that you got. 
Lets say that we are transmitting two bits, either a 1 or a -1 each. 

Given 4 multivariate(two dimensional) gaussian models $\mu _{i}, \Sigma _{i}$, for $i=1,2,3,4$ where
$$
\begin{align}
M_{1} = \begin{bmatrix}
1\\1
\end{bmatrix}, M_{2} = \begin{bmatrix}
1\\-1
\end{bmatrix}, M_{3} = \begin{bmatrix}
-1\\1
\end{bmatrix}, M_{4}=\begin{bmatrix}
-1\\-1
\end{bmatrix}
\end{align}
$$
These have different means, but the same covariance matrix
$$
\begin{align}
\Sigma= \begin{bmatrix}
1 & 0\\0 & 1
\end{bmatrix}
\end{align}
$$
What is the most likely message if I received
$$
\begin{align}
x = \begin{bmatrix}
0.5 \\ -0.2
\end{bmatrix}
\end{align}
$$
It is immediately obvious to the casual observer upon first inspection on a plot
![[Pasted image 20260226101739.png|300]]
Let's do the math
$$
\begin{align}
f(x | \mu _{i}) = \frac{1}{\sqrt[]{ (2\pi)^{2} \cdot 1 } } e^{\frac{-1}{2}(x-\mu _{i})^{T}(x-\mu _{i})}
\end{align}
$$
We want to find the argument $\mu _{i}$ that maximizes that expression. 

We can take the natural log without changing the thing that will make the maximum. Really, were looking for the argmax of
$$
\begin{align}
\ln \frac{1}{\sqrt[]{ (2\pi)^{2} } } - \frac{1}{2}\cdot \left| \left| x-\mu _{i} \right|  \right|_{2}  ^{2}
\end{align}
$$
We just have to look at whichever gaussian's mean has the smallest Euclidean distance (this is the L2 norm). 
