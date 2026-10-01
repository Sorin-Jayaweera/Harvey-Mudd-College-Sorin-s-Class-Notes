We take a non negative matrix $\mathbb{R}^{k\times n}$ and decompose it into a $\mathbb{R}^{k\times R}\cdot \mathbb{R}^{R\times n}$
where $R$ is much smaller than the rank of $v$. 

This is just the assumption that we don't have harmonic spikes that destructively interfere. Only constructive interference, because we only allow positive elements. 

![[Pasted image 20260331101614.png]]


## problem formulation
lets try to approximate the nonnegative matrix $v$ as a product of $w$ and $h$.

We are finding the argmin of $w\text{ and } h$. We want to find the best reconstruction. I.e. minimize the reconstruction loss $\lvert v-WH \rvert^{2}$
This is the Frobenius norm.

$$
\begin{align}
\left| A \right| ^{2} = \sum_{i=1}^{R} \sum_{c=1}^{C} \left| A_{rc}  \right| ^{2} 
\end{align}
$$

We don't know what $w$ and $H$ are, but they have to be nonnegative. There is no analytical solution for this right now.
>[!bug] We DON'T have the case
>$$
>\begin{align}
>A\geq 0 
>\end{align}
>$$
>since that means $x^{T}Ax\geq 0$ (positive semidefinite). 
>We have the condition that every element in the matrix is non negative,
>$A_{rc}\geq 0\,\forall r,c$


Lets break this into an easier problem.

If $W$ is fixed, $f(H)= \left| V-WH \right|^{2}$ is convex
If $H$ is fixed, $f(W)= \left| v-WH \right|^{2}$ is convex
(bowl).

We can fix one matrix and set the derivative to zero, then find the minimum easily. 
>[!abstract]+ Insight!
>We can guess one matrix and solve for the second, then use that to solve the first. We can continue this iteration until we have the globally optimal solution! this is like newtons method


>[!abstract]+ Insight
>If we know the gradient, we can improve the estimate.
>Iterative approach towards optimization - we go towards the gradient descent for a step, then find the gradient, and go for another step, etc. We almost never have convex problems in the real world.
> pick $h^(0)$ randomly
>``` python 
>for i in range(numiterations):
>
>```
>$h^{(i+1)}= h^{(i)}- \gamma\cdot \frac{ d e}{d h }\bigg|_{h=h^{(i)}}^{}$
>Where $h^{(i+1)}$ is the updated estimate
>$h^{(i)}$ is the current estimate
>$\gamma$ is the distance to step (learning rate)
>$\frac{ \partial e }{ \partial h }$ is the gradient of the error with a parameter
>evaluating the gradient at the current estimate



>[!example]+  Use gradient descent to minimize $y=x^{2}$
>Plot $x^{(i)}$ estimates for $\gamma=0.1,-.7,\text{ and } 0.15$. This is an easy problem, but lets see
>assume $x^{(0)}=10$. Lets plot the sequence of estimates for three different learning rates. 
>
>$$
>\begin{align}
>x^{(i+1)} & =x^{(i)}-\gamma \frac{ d y}{d x }\bigg|_{x=x^{(i)}}^{} \\
> & = x^{(i)}- \gamma\cdot 2x^{(i)} \\
> & = (1-2\gamma)x^{(i)}
>\end{align}
>$$

![[Pasted image 20260331105146.png|400]]




For a matrix variable,

We pick $H^{(0)}$ randomly

for i in range(numiterations)
	$H^{(i+1)}= H^{i} - \gamma \cdot \frac{ d e}{d H }\bigg|_{H=H^{i}}^{}$

Where 
$$
\begin{align}
H^{i+1} \text{ and } H^{(i)} \text{ look like } \\
\begin{bmatrix}
H_{11} &  H_{12}  & \dots  & H_{1N} \\
H_{21} &  \dots \\
\vdots  & \\
H_{R_{1}} &  \dots  & \dots  & H_{RN}    
\end{bmatrix}
\end{align}
$$

are $\mathbb{R}^{R\times N}$ matrices. 
$\gamma$ is a scalar
$$
\begin{align}
\frac{ d e}{d H } = \begin{bmatrix}
\frac{ d e}{d H_{11}  }  & \frac{ d e}{d H_{12}  }  & \dots & \frac{ d e}{d H_{1N}  }  \\
\vdots \\
\frac{ d e}{d H_{R_{1}}  }  & \dots & \dots &  \frac{ d e}{d H_{RN}  } 
\end{bmatrix}
\end{align}
$$

>[!example]+  Derive gradient descent update for minimizing
>(a) $f(H)= \left| V-WH \right|^{2}$
>(b) $f(W)= \left| v-WH \right|^{2}$
>useful facts:
>$\left| A \right|^{2}= tr(A^{T}A)$
>$tr(A+B)=tr(A)+tr(B)$
>$tr(\underbrace{ A }_{ N\times N })= \sum_{i}^{n}A_{i} = tr(A^{T})$
>$tr(AB)=tr(BA)$
>$\frac{ d }{ dA }tr(A^{T}B)=B$
>We want to find the frobenius norm, we express that as the trace of the matrix $A^{T}A$ (since that is just the sum of squares of the matrix)


$$
\begin{align}
\frac{ d f}{d H }  & = [\left| V-WH \right| ^{2}] \\
 & = \frac{ \partial  }{ \partial H } [tr((V-WH ^{T})(V-WH ))]  \\
 & = \frac{ \partial  }{ \partial h } [tr(V^{T}V)- tr(V^{T}WH)- tr(H^{T}W^{T}V)+ tr(H^{T}W^{T}WH)] \\
 & = \frac{ \partial  }{ \partial h } tr(V^{T}V) - \frac{ \partial  }{ \partial H } tr(V^{T}WH)- \frac{ \partial  }{ \partial H } tr(H^{T}W^{T}V)+ \frac{ \partial  }{ \partial H } tr(H^{T}W^{T}WH) \\
 & = 0 - \frac{ \partial  }{ \partial H } tr(H^{T}W^{T}V)- \frac{ d }{d H } tr(H^{T}W^{T}V)+ \frac{ d }{d H } tr(H^{T}W^{T}WH) \\
 & = -W^{T}V - W^{T}V + 2W^{T}WH \\
 & = 2 (W^{T}WH-W^{T}V)
\end{align}
$$
so
$$
\begin{align}
H^{(i+1)}= H^{(i)} - \gamma(W^{T}WH^{i}-W^{T}V)
\end{align}
$$



Similarly, for $\frac{ \partial f }{ \partial W }$

$$
\begin{align}
& = \frac{ \partial  }{ \partial h } tr(V^{T}V) - \frac{ \partial  }{ \partial H } tr(V^{T}WH)- \frac{ \partial  }{ \partial H } tr(H^{T}W^{T}V)+ \frac{ \partial  }{ \partial H } tr(H^{T}W^{T}WH)   \\
 & = 0 - \frac{ d }{d w } tr(W^{T}VH^{T}) - \frac{ d }{d W } tr(W^{T}VH^{T})+ \frac{ d }{d W } tr(W^{T}WHH^{T}) \\
 & = -VH^{T}-VH^{T}+2WH H^{T} \\
 & = 2(WHH^{T}-VH^{T}) \\
\end{align}
$$

Which gives the learning rule
$$
\begin{align}
W^{(i+1)} & = W^{(i)}- \gamma(W^{(i)}H H^{T} - VH^{T})
\end{align}
$$
We repeat until convergence. However, we can't stop here - this doesn't garuntee non-negativity!


>[!abstract]+ Insight
>We can enforce non-negativity with a multiplicative update, using an adaptive learning rate
>$\gamma^{(i)}_{rn}$ instead of a global scaler $\gamma$.
>$\gamma_{rn}^{(i)} = \frac{H^{(i)}_{rn}}{(W^{T}WH^{(i)})_{rn}}$ when estimating $H$
>$\gamma_{kr}^{(I)}= \frac{W_{kr}^{(i)}}{(W^{(i)HH^{T}})_{kr}}$ when estimating $W$

We are multiplying on each update instead of adding and subtracting - and if they are always positive, then we will never get to a negative!

Lets derive the update rule for $H$ and $W$
$$
\begin{align}
H^{(i+1)}_{rn}  & =  H^{(i)}_{rn} - \gamma_{rn} ^{(i)} ( (w^{T}WH^{(i)})_{rn} - (W^{T}V)_{rn} ) \\
 & = H^{(i)}_{rn} - \frac{H_{rn}^{(i)} }{(W^{T}WH^{i})_{rn} } ((W^{T}WH^{(i)}- (W^{T}V)_{rn} )) \\
 & = H^{(i)}_{rn} \cdot \frac{(W^{T}V)_{rn} }{(W^{T}WH^{(i)})_{rn}} 
\end{align}
$$

Lets write this in the vectorized form
$$
\begin{align}
H^{(i+1)}= H^{(i)} \odot    W^{T}V \underbrace{ ⊘ }_{ \text{ elementwise divide }}W^{T}WH^{(i)}
\end{align}
$$
The update rule for $W$ is
$$
\begin{align}
W^{(i+1)}= W^{(i)} \odot   VH^{T} ⊘W^{(i)}H H^{T}
\end{align}
$$

![[Pasted image 20260402103106.png]]
The product of non negative values is non negative
we can prove that error is non-increasing [lee and seving 20000]

We ensure non negativity by using carefully chosen adaptive learning rates

## THE ALGORITHM

### overview
$$
\begin{align}
\text{ We  }\underbrace{ \text{ alternate  } }_{ \text{ insight 1 } } \text{ between} \underbrace{ \text{  gradient descent } }_{ \text{ insight 2 } } \underbrace{ \text{with multiplicative updates
 } }_{ \text{ insight 3 } }
\end{align}
$$
The pseudo code:

We initialize $W^{(0)}$ and $H^{(0)}$ - 

for i in range(numiiterations):
$$
\begin{align}
H^{(i+1)} & = H^{(i)}\odot   W^{(i)T}V ⊘  W^{(i)T}W^{(i)}H^{(i)} \\
W^{(i+1)} & = W^{(i)} \odot  VH^{(i+1)T} ⊘ W^{(i)}H^{(i+1)}H^{(i+1)T}
\end{align}
$$

### Initialization

With multiplicative updates, a zero remains zero forever
we can incorperate prior knowledge by setting elements to be zero
initialization is problem dependent

Lets think about the template matrix $W$

#### Initializing W
On a piano you know in advance what the notes are / how many, so we can choose the width of the matrix (number of states) and *set the non harmonic frequencies to zero.*

We initialize a band around $f_{0}$, as $f_{0}-\Delta f$ and $f_{0}+\Delta f$ - initializing those all as nonzero, and zero everywhere else. *We have to propagate that band forwards to the harmonics, i.e. $2(f_{0}+\Delta f), \,\,3(f_{0}+\Delta f)$*
We expect the fundamental frequency to be within that range, but outside the bands we want it to be zero.
![[Pasted image 20260402104155.png]]

#### Initializing H
If the music score is available, we can determine note-level alignment using DTW.

We can impose time constraints on where templates are active
we add margins to handle alignment inaccuracies

![[Pasted image 20260402104207.png]]
 
#### Other
![[Pasted image 20260402104639.png|300]]


## Reconstruction

We can split the notes into left and right hand, computing $WH^{L}\text{ and } WH^{R}$, which we estimated the magnitude STFTs.
Use phase from $\chi$, and do ISTFT.

### Better approach
compute soft masks - find how much energy comes from the left hand
$$
\begin{align}
M^{L}= WH^{L} ⊘ (WH+\underbrace{ \epsilon }_{ \text{ avoid division by 0 } })  \\
M^{R} = WH^{R} ⊘ (WH+\epsilon)
\end{align}
$$

We then apply masks
$$
\begin{align}
\hat{\chi}^{L}= M^{L} \odot  X \\
\hat{X}^{R} = M^{R} \odot  X
\end{align}
$$
Then we do the inverse STFT. 
