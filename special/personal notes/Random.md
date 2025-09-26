$$
\begin{align}
 \text{ let } Z_{eq}= \frac{Z_{\text{ load }}Z_{2}}{Z_{\text{ load }}+Z_{2}}\\
V_{op}=V_{in} \frac{Z_{eq}}{Z_{1}+Z_{eq}} \\
V_{om}=V_{in} \frac{Z_{eq}}{Z_{1}+Z_{eq}} \\
\delta{n}= \frac{ \partial  }{ \partial \text{ var } } \frac{\frac{Z_{\text{ load }}Z_{2}}{Z_{\text{ load }}+Z_{2}} }{Z_{\text{ load }+\frac{Z_{\text{ load }}Z_{2}}{Z_{\text{ load }}+Z_{2}} }}\\ \\
\lambda= \sqrt{ \sum_{n=0}^{} (\delta n \underbrace{ \epsilon_{n}}_{ \text{ confidence of equipment } })^{2}  } \\
\text{ where n describes } [Z_{1},Z_{2},Z_{\text{ load }}] \\
\text{ \% error } = \frac{v_{op} -v_{om}}{v_{om}}100 \% 
\end{align}
$$




## OP Amps

$$
\begin{align}
V_{in,\text{ rms }} = \frac{v_{pp}}{2\sqrt{ 2 }} \\
V_{\text{ in, par}} = \frac{z_{2}}{z_{2}+z_{1}} \\
Z_{n,\text{ par }} =  v_{in} \frac{d}{dz_{n}}\left( \frac{z_{2}}{z_{1}+z_{2}} \right)  \\
v_{op}=v_{in}\frac{z_{2}}{z_{1}+z_{2}} \\
\text{ Assuming the op amp is operating efficiently } \\
\text{ and has no input impedance: } \\
z_{n,\text{ par }} = \frac{ \partial  }{ \partial z_{n} } \frac{z_{2}}{z_{1}+z_{2}} v_{in} \\
\lambda= \sqrt{ \sum_{n=0}^{} (\delta n \underbrace{ \epsilon_{n}}_{ \text{ confidence of equipment } })^{2}  } \\
\text{ where n describes } [Z_{1},Z_{2}] \\
\text{ \% error } = \frac{v_{op} -v_{om}}{v_{om}}100 \% 
\end{align}
$$


