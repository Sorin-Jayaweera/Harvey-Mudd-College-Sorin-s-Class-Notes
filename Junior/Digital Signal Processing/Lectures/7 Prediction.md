## Viterbi

Given observations and a trained model, lets estimate the states.

Given observations in time and a hidden Markov model, determine the most likely state sequence. 

The model $\Theta$ which maximizes the chance of getting the observations $o$ from a sequence of states $s$ is the "best" one. 
At every time step, consider the total number of states that you could be in. 

If there are $n$ time steps and $i$ states, we have $i^{n}$ combinations to search. This is not tractable. 

$$
\begin{align}
S^{*} = \text{ argmax }(P(o,s | \Theta))
\end{align}
$$
We have
$$
\begin{align}
P(o,s)  & = P(o_{1},\dots,o_{N} )  \\
 & = P(S_{1})P(o_{1}|S_{1})P(S_{2}|PS_{1},O_{1})P(O_{2}|S_{2},d_{1},O_{1})P(S_{3}|S_{2},O_{2}S_{1}O_{1} \\
 & = P(S_{1})P(O_{1}|S_{1})P(S_{2}|S_{1})P(O_{2}|S_{2})P(S_{3}|S_{2})\dots \\
 & = P(S_{1})P(O_{1}|S_{1})\cdot \prod_{n=2}^{N} P(s_{n}|S_{n-1}  )P(O_{n}|S_{n})
\end{align}
$$

$$
\begin{align}
\ln (P(O,S))= \underbrace{ \ln P(s_{1})+\ln  P(O_{1}|S_{1}) }_{ \text{ initialize } } + \underbrace{ \sum_{n=2}^{N}( \ln P(s_{n}|s_{n-1})+ \ln P(o_{n}|s_{n})) }_{ \text{ transitions } }
\end{align}
$$

We can rephrase this to finding the highest scoring path through a matrix.

We are now computing the pairwise similarity matrix and et the path with the highest score. 

The similarity matrix is $\mathbb{R}^{\mathbf{I}\times \mathbf{N}}$
For example, the multivariate gaussian


| $\alpha_{i}$ | $P(o_{1}\|\alpha_{I})$ |                        |         |         |         |
| ------------ | ---------------------- | ---------------------- | ------- | ------- | ------- |
| $\vdots$     | $\vdots$               |                        |         |         |         |
| $\alpha_{2}$ | $P(o_{1}\|\alpha_{2})$ | $\urcorner$            |         |         |         |
| $\alpha_{1}$ | $P(o_{1}\|\alpha_{1})$ | $P(o_{2}\|\alpha_{1})$ |         |         |         |
|              | $o_{1}$                | $o_{2}$                | $o_{3}$ | $\dots$ | $o_{n}$ |
In this case, we can be in any state at any time. We are moving between each time step observation from left to right, but with the maximum probabilities. 



The transition score is often modified to
$$
\begin{align}
\ln P(s_{n}|s_{n-1} )+ \underbrace{ \lambda }_{ \text{ hyper parameter } } \cdot \ln  P(o_{n}|s_{n}) \\
\end{align}
$$


## Learning Model
Given observations and states, how do we train a model?

Lets say we have a bunch of observations $O=(O_{1},O_{2},O_{2},\dots)$, and the state sequence that it actually corresponds to. 

We need the state transitions, and the parameters of a Gaussian. Each model is given by
$$
\begin{align}
\Theta = (A,\Pi,\mu_{1},\mu_{2},\dots, \Sigma_{1},\Sigma_{2},\dots)
\end{align}
$$
Where $A$ is the state transition matrix and $\Pi$ is the probability of starting in a state. 

### A
The transitions are given as
$$
\begin{align}
a_{ij} = \frac{\tilde{a}_{ij}}{\sum_{j}^{} \tilde{a}_{ij}} 
\end{align}
$$
### $\Pi$
The initial state probability is either
* manual
* averaged over all the states
* averaged over all first states


### $\mu _{i}$ 
The average of all observations from the state $\alpha _{i}$

### $\Sigma _{i}$
$$
\begin{align}
\Sigma _{i}= \frac{1}{N_{i}-1} \sum_{D=0}^{N_{i}} (x_{i}^{n}-\mu _{i})(x _{i}^{n}-\mu _{i})^{T}
\end{align}
$$
This is computing an outer product, since the dimensions are
$$
\begin{align}
\mathbb{R}^{D\times 1}\times \mathbb{R}^{1\times D}  
\end{align}
$$
