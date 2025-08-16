Probabilities assume a stochastic/random process with multiple outcomes, and are the chance of a(n) set of outcomes out of the total. The #probability of an outcome is the fraction of times the outcome would occur if we observed the experiment **infinitely** many times. They lie from $0\leq P\leq1$ inclusive.

We can only estimate a probability by using a finite number of samples. If we flip a coin 100 times, it could have 50 times on each side. But it could also land 100 times on one side. The larger the number, the more that we approach the true probability distribution. 

A #sample_space (denoted $S$) of an experiment is the set of all possible outcomes of the experiment.
An #event is any subset of a sample space, usually denoted by an $A$.
The #compliment of $A$ is $A^{c}$, which is everything outside of that sample space. $A^{c}=S-A$
![[Pasted image 20240826140841.png|450]]
An example sample space S for flipping a coin three times is
$$
\begin{align}
S = \left\{ H H H, H H T, H T H, T H H.. T T T \right\}
\end{align}
$$
(There are 8 possibilities. 2 options for each flip and for each of those, there are the other flips. There are 3 flips, so $2\times 2\times 2 = 2^{3}=8$)

We can express these two sets with set logic.
The union of sets $A\text{ and } B$, this is $A\cup B$.
The intersection of sets $A \text{ and } B$ is $A\cap B$.
![[Pasted image 20240826141151.png|450]]
Events $A \text{ and } B$ are disjoint of $A\cap B=0=\left\{  \right\}$

$P\left( A\cap B \right) =$ The probability that an outcome is in $A\cap B$.
If $A\text{ and } B$ are disjoint, $P(A\cap B)=0.$

$$
\begin{align}
P(A\cup A^{c})=1\\
P(A\cap A^{c})=0 \\
\end{align}
$$
We have rules under which we can express arithmetic under probability functions.
The compliment rule:
$$
\begin{align}

P(A\cup A^{c})=1  \\
\text{ Can be rewritten as} \\
P(A)=1-P(A^{c})
\end{align}
$$
The addition rule:
If $A_{1},A_{2},\dots,A_{n}$ are of **disjoint** events, then $P(A_{1}\cup A_{2}\cup\dots \cup A_{n})=P(A_{1})+\dots+P(A_{n}).$
We can only add if we don't have overlap. Otherwise, we would have to account for double counting sets.

If the events are not disjoint, we have to subtract the intersection between those sets. Thus, more generally
$$
\boxed{
\begin{align}
P(A_{1}\cup A_{2})=P(A_{1})+P(A_{2})-P(A_{1}\cap A_{2})
\end{align}
}
$$


Two random processes are independent if knowing the outcome of one provides no information about the other. This gives us the multiplication rule.
If $A_{1},A_{2},\dots,A_{k}$ are events from independent processes, then chance of any set of outcomes between that set of processes is $A_{1}*A_{2}*\dots*A_{k}$
This is formalized as
$$
\begin{align}
P(A_{1}\cap \dots \cap A_{k})=P(A_{1})P(A_{2})\dots P(A_{k})
\end{align}
$$
Lets take a tricky example. Imagine two teams are playing three rounds of a game, and two wins are required to beat the other team. If team 1 has a $0.6$ chance of winning each game, and the games are independent, what is the chance that the team wins?
The answer is not $0.6^{2}$. They could win the first two games, or they could loose one game and win either the first and last or the second two.

Thus, their chance of winning is 
$$
\begin{align}
0.6^{2}+2*0.6^{2}*0.4
\end{align}
$$
If we have three events, 
$$
\begin{align}
P(A\cup B\cup C)=P(A\cup(B\cup c) = P(A)+P(B\cup C)-P(A\cap(B\cup C)) \\
A \cap(B\cup C)=(A\cap B)\cup(A\cap C)
\end{align}
$$








