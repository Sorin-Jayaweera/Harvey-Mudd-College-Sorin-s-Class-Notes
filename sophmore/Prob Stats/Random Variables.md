---
lecture: math-56-4
tags:
  - Random_variables
  - distribution
  - sample_space
aliases: 
cssclasses:
---

##### _definition_: Random Variable
A random variable isa variable whose values depend on outcomes of a random process. Random variables can be though of as functions with inputs "outcome in a sample space" and outputs "numerical value".
 Notation: Capital letters near the end of the alphabet: E.G. $X,Y,Z$.
$$
\begin{align}
X=\text{ outcome of a coin flip } \\
Y= \text{ \# of students absent today } \\
z = \text{ time spent waiting for uber }
\end{align}
$$
Random variables follow a #distribution, the probability of each outcome or value from that process.

We want to know the range of values, aka the #sample_space , the mean, median, mode, kurtosis of the distribution, expected value, variance, expected value, standard deviation, etc.

Expected value: the average value, NOT the value with the highest probability. Flipping a coin heads(1) and tails(0) has an expected value 0.5.

Discrete probability distributions are called probability mass functions, whereas continuous functions are called probability density functions.

##### _Definition:_ #Expected_value


For a 6 sided dice, the expected value is 
$$
\underset{  }{ \begin{align}
1*\frac{1}{6} + 2* \frac{1}{6} + \dots + 6\frac{1}{6} \\
= (1+2+3+4+5+6)\left( \frac{1}{6} \right) \\
= (7*3)\left( \frac{1}{6} \right) \\
= \frac{21}{6} \\
\end{align} }
$$

Expected value is a linear operator, so 
$$
\begin{align}
E(X)+E(Y)=E(X+Y) \\
E(aX)=aE(x) \\
E(a)=a
\end{align}
$$
For a constant a.

##### _Definition_ #Variance 
Variance of a discrete random variable is
$$
\begin{align}
\sum_{i=1}^{k}(x_{i}-\mu)^{2}\cdot p(x=x_{i}) = E((x-\mu)^{2})
\end{align}
$$
This is "how far from the average is the variable expected to be"
V(X) is a measure of the variability/volatility of a random variability, and is often denoted $\sigma^{2}$. The standard deviation $\sigma$ is the square root of the variance.

To compute variance, we typically use the "shortcut" formula:
$$
\begin{align}
V(x) & = 
E(x^{2})-E(x)^{2}\\ & =E(X^{2})-\mu^{2}
\end{align}
$$
$$
\begin{align}
V(x+y)=V(x)+V(y) \\
V(aX)=a^{2}V(x) \\
\end{align}
$$



##### Definition #Bernoulli_random_variable
takes one of two values: success with probability p or failure with probability 1-p

A geometric distribution: If the probability of success in each trial is p, and the probability of failure is 1-p, then the probability of the first success occurring on the nth trial is $(1-p)^{n-1}p$.
A geometric distribution is memoryless, so each trial is independent of past and future trials. Each event is a called a Bernoulli trial.
$$
\begin{align}
\mu=\frac{1}{p}, \sigma^{2}=\frac{1-p}{p^{2}}
\end{align}
$$




##### Definition #Binomial_distribution:
describes the number of successes $k$ in a sequence of $n$ Bernoulli trials. To denote that a random variable $X$ follows the binomial distribution, we use $X~ B(n,p)$. The probability mass function is given by 
$$
\begin{align}
P(k;n,p):=P(X=k)= \left( n\choose  k \right) p^{k}(1-p)^{n-k} 
\end{align}
$$
$$
\begin{align}
\mu=np,\sigma^{2}=np(1-p)
\end{align}
$$



##### Definition #Poisson_distribution
A probability distribution for the number of events occurring in a fixed time interval. We use the Poisson distribution when the following assumptions hold: 
1) The occurrence of one event does not affect the probability that a second event will occur(i.e. events occur independently)
2) The average rate that events occur is constant
3) Two events can't occur at the same time ( i.e. in each very small unit of time, 0 or 1 events occur.
Suppose we are watching for events that follow a Poisson distribution with average rate $\lambda$ per time $T$. Then, in the time interval $[t,t+T]$, the probability that we observe exactly $k$ events is 
$$
\begin{align}
P(k)=\frac{\lambda^{k}e^{-k}}{k!}  \\ \\
\text{ we also have the following neat properties: } \\
\mu=\lambda \\
\sigma^{2} =\lambda
\end{align}
$$



