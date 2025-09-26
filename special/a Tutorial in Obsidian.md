Quick Latex origional file:
bi:::\binom{#cursor}{#tab};
sq:::\sqrt{};
bb:::\mathbb{};
bf:::\mathbf{};
te:::\text{};
inf:::\infty;
cd:::\cdot;
qu:::\quad;
ti:::\times;
al:::\alpha;
be:::\beta;
ga:::\gamma;
Ga:::\Gamma;
de:::\delta;
De:::\Delta;
ep:::\epsilon;
ze:::\zeta;
et:::\eta;
th:::\theta;
Th:::\Theta;
io:::\iota;
ka:::\kappa;
la:::\lambda;
La:::\Lambda;
mu:::\mu;
nu:::\nu;
xi:::\xi;
Xi:::\Xi;
pi:::\pi;
Pi:::\Pi;
rh:::\rho;
si:::\sigma;
Si:::\Sigma;
ta:::\tau;
up:::\upsilon;
Up:::\Upsilon;
ph:::\phi;
Ph:::\Phi;
ch:::\chi;
ps:::\psi;
Ps:::\Psi;
om:::\omega;
Om:::\Omega


> [!abstract]+ Theorem
sdf
sdf> 




make a new note that is linked: [[]]
ie: ill choose [[op1]] instead of [[op2]]

6 keys to markdown
The Link. [[]]
The tag. Lets use #concept 
#redpill
Italic.  *words are cool*, surrounded with * *
Bold.  **big words** surrounded with ** **
Strikethrough ~~mistake~~ with ~ ~
# header 
more # .mean more header forms
# Hotkeys:
toggle preview cmd e
quick switcher: cmd o 
Search: cmd shift f 
Back: cmd opt leftArrow ?
New note: cmd n
Note in new pane: cmd click on note
- [ ] ctrl L make a box or mark it done
 

# Graphs:
```tikz
\usepackage{tikz-cd}
\begin{document}
	\begin{tikzcd}
	u \ar [rrd,"u" ]& v & z\\
	a & b & c
	\end{tikzcd}
\end{document}
```
# Math:

Enter math mode with d m 
- "xsr" → "x^{2}".
$$
x^{2}
$$
- "x/y Tab" → "\frac{x}{y}".
- $$
\frac{x}{y}
$$
- "sin @t" → "\sin \theta".
$$
\sin\theta

$$
$$
\frac{ \partial f }{ \partial x } 
$$

$$
\int_{0}^{2\pi} \sin\theta \, d\theta 
\int_{-\infty}^{\infty}  \, dx 
\infty sixty two
$$

typing "par Tab f Tab x Tab" → "frac{partial f}{partial x}".
typing "dint Tab 2pi Tab sin @t Tab @t Tab" → "int_{0}^{2pi} sin theta , dtheta".

Sometimes you want to annotate math, or cancel or cross out terms. Selecting some math with the cursor and typing
shift + 
- "U" will surround it with "\underbrace".
- "C" will surround it with "\cancel".
- "K" will surround it with "\cancel to".
- "B" will surround it with "\underset".

$$
\underbrace{ \int_{0}^{2\pi} \frac{2xy}{3\sum_{0}^{3} {\frac{2x}{5}}} \, dx  C }_{  }
\cancel{ \int_{0}^{2\pi} \frac{2xy}{3\sum_{0}^{3} {\frac{2x}{5}}} \, dx } 
\cancelto{  }{ \int_{0}^{2\pi} \frac{2xy}{3\sum_{0}^{3} {\frac{2x}{5}}} \, dx  C }
\underset{  }{ \int_{0}^{2\pi} \frac{2xy}{3\sum_{0}^{3} {\frac{2x}{5}}} \, dx  C }
	$$
$$
\begin{bmatrix}
rx & ry & yz &  \\
s_{1} & s_{2} & s_{3} \\
\end{bmatrix}
\begin{matrix}
s_{1} & s_{2} & s_{3} \\
\psi & \theta & \rho  \\
\pi & \alpha & \theta \\
\rho & \sigma & \Sigma \\
 \epsilon  \\ \\

\end{matrix}
$$
thus you have something like
$$
\begin{array}
 & a & b & c & d &  \\
d & 3
\end{array}
$$

$$
\begin{bmatrix}
\vec{a} \\
\vec{b}
\end{bmatrix}
$$
| Header 1 | Header 2 | Header 3 |  
| -------- | -------- | -------- |  
| Item 1 | Item 2 | Item 3 |  
| Item 4 | Item 5 | Item 6 |

Images can just be pasted  
![[Pasted image 20240117093933.png]]

$$
\begin{align}
1 == 1 \\
2 == 2 \\

\end{align}
$$
$$
\begin{align}
a&=b \\
a&=b \\
&=c \\

\end{align}
$$

$$
\int_{0}^{2\pi} fx \, dx 
$$





