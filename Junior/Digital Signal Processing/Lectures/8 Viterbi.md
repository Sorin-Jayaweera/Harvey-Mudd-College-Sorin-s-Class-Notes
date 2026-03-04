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
