
The conditional probability of an event $A$ occurred given that another event $B$ occurred. The event $B$ is called the conditioning event.
Notation: We say "The probability of A given B" is $P(A|B)$

As an example: Assume a 20% chance of getting into a college, and a 3% chance of getting a scholarship. The chance of getting a scholarship given that you are accepted is 3%, but the overall probability is 0.006%. 

We can use Bayes' Theorem.
We can write out 
$$
\begin{align}
P(A\cap B)=P(A|B)*P(B)
\end{align}
$$
If $A$ and $B$ are independent, then knowing the outcome of $B$ gives no information about the outcome of $A$. So intuitively, we can conclude that $P(A|B)=P(A)$.

Example. Suppose there's a test for a disease that's $99$ % reliable, i.e. 99% of people with the disease test positive and 99% of healthy people test negative. If 1% of people taking the test actually have the disease, what's the probability that a positive test means the patient has the disease?
This can be written as 
$$
\begin{align}
P(disease|positive)=\frac{P(Positive \cap disease)}{P(positive)}\\
\end{align}
$$

We know that $P(Positive \cap \text{ has disease })=0.01*0.99$
and that $P(\text{ positive })=P(\text{ disease and positive })+P(\text{ no disease and positive  })$
To get the final result 50%.

The law of total probability:
Suppose that the sample space $S$ consists entirely of the disjoint events $A_{1},A_{2},\dots,A_{k}$. Then, for any other event $B$,
$$
\begin{align}
P(B)=P(B|A_{1})*P(A_{1})+P(B|A_{2})P(A_{2})+\dots+P(B|A_{k})P(A_{k})
\end{align}
$$



