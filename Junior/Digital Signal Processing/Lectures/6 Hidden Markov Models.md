Lets build a toy "speech recognizer" that can recognize "Yes" and "No" in any sequence. This is the basic system that was "state of the art" until 2010 ish (sequence models took over). 

Hidden Markov models infer state from a sequence of observations. 

## Definitions

Set of possible states $\mathcal{A}= \left\{ \alpha_{1},\dots, \alpha _{n} \right\}$
* In the speech recognizer, this is the sounds that you could say. 
* I.e. "Yes" and "No" are words, but the distinct states are the unique sounds: "y", "eh", "s", "n", "oh", and silence ("sil"). These 6 phonemes are all the possible states.  The number of states $I$ is 6.
State sequence $s_{1},s_{2},s_{3}\dots$
* y, y, y, eh, eh, s, s, s, sil, siil

Markov property: $P[S_{n+1}= \alpha_{j}|s_{n} = \alpha_{i}, s_{n-1} = \alpha_{k},\dots]=P[s_{n+1}=\alpha_{j} | s_{n}= \alpha_{i}]$
* The next state only depends on the current state, not the past
Markov chain: a system that is Markov and time-invariant
* $$
\begin{align}
P[s_{n+1} &  = \alpha_{j} | s_{n} = \alpha_{i} , s_{n-1} = \alpha_{k} ,\dots ] \\
 &  = P[s_{n+1}= \alpha_{j} | s_{n}= \alpha_{i}   ]  \\
 & = a_{ij} \text{ a constant - time invariant! }
\end{align}
$$
$a_{ij}$ is the probability that given you are in I then you go to state J. 


We have a state transition matrix, of size $I\times I$.
$$
\begin{align}
A = \begin{bmatrix}
a_{11}  & a_{12}  &\dots &  a_{1I}  \\
a_{21}  & a_{22}  &\dots &  a_{2I}  \\
\dots \\
a_{I1}  & a_{I2}  &\dots &  a_{II} 
\end{bmatrix}
\end{align}
$$
This is a PMF - the sum of entries in one row is equal to 1. 

Initial state probabilities
* we have a chance of being in any of the starting states
$$
\begin{align}
\Pi_{i}  & = P[s_{1}=\alpha _{i}] \\
\Pi  & = [\pi_{1}, \pi_{2}, \dots,\pi_{I} ]  
\end{align}
$$

We can draw a markov chain in a graph
![[Pasted image 20260226104628.png|300]]

We can build a state transiton matrix with rows in order C, F, G
$$
\begin{align}
S=\begin{bmatrix}
0.8 & 0.1 & 0.1 \\
0.1 & 0.6 & 0.3 \\
0.2  & 0.1 & 0.7
\end{bmatrix}
\end{align}
$$
If we take an initial state with some probability of being on any of the nodes, we can go forwards one state
$$
\begin{align}
[\pi_{c}\,  \pi_{F} \, \pi_{g}  ] S = [P(s_{2}=c) \, P(s_{2}=F) \, P(s_{2}=g)]
\end{align}
$$
We can find the probability for any time point as
$$
\begin{align}
[\pi_{c}\,  \pi_{F} \, \pi_{g}  ] \cdot S^{n}= [P(s_{n+1}=c) \, P(s_{n+1}=F) \, P(s_{n+1}=g)]
\end{align}
$$

