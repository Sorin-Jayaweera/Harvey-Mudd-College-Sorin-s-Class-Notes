---
tags:
  - Phys51
---
#### Circuit Rules
- Kirchhoff's Law/Loop Rule ([[Conservation of Energy]]): 
	The sum of [[special/FriendsNotes/Phys51/Electrostatic Potential|potential]] differences around a closed loop equal to zero. $$
\underset{ \text{loop} }{  \sum_{\text{around}} } \Delta V = 0$$
- [[Charge]] Conservation:
	For any node in a circuit, the total [[Current]] flowing into the node must be equal to the total current leaving it. $$
\sum i_{in} = \sum i_{out}
$$

([[Higher Order ODEs#Example 2]], [[Second Order ODEs]])

**Example 1:**
![[Pasted image 20240924102202.png|400]]
$$
\sum\Delta V = 0
$$
$$
\implies (V_{b}-V_{a}) + (V_{c}-V_{b}) + (V_{d}-V_{c})+ (V_{a}-V_{d}) = 0
$$
$$
= +V_{0} + 0 - iR_{1} -iR_{2} \implies V_{0} = i(R_{1}+R_{2}) = iR_{eff}
$$

**Example 2:**
![[Pasted image 20240924102413.png|300]]

For top loop:
$$
\sum\Delta V = 0
$$
$$
+V_{0}-i_{1}R_{1} = 0 \implies i_{1} = \frac{V_{0}}{R_{1}}
$$
For bottom loop:
$$
+V_{0}-i_{2}R_{2} \implies i_{2} = \frac{V_{0}}{R_{2}}
$$
$$
i = i_{1}+ i_{2} = V_{0}\left( \frac{1}{R_{1}} +\frac{1}{R_{2}}\right) 
$$
$$
V_{0} = iR_{equiv} = i\left( \frac{1}{R_{1}}+\frac{1}{R_{2}} \right)^{-1}  
$$


**Battery Voltage**: $V_{0}$ or $\epsilon$.


Work by battery:
$$
W_{\text{on }+q} = qV_{0}
$$
Power from battery:
$$
P = \frac{d}{dt}(W) = \frac{d}{dt}(qV_{0}) = iV_{0}
$$
Power from charges into resistor: $$
P_{dissipated} = \frac{d}{dt}(W) = \frac{d}{dt}(q\Delta V) = i\Delta V = i^{2}R 
$$([[Ohm's Law]])
For any circuit component:
$$
P_{component}  = i\Delta V
$$


**Example 3:**
![[Pasted image 20240924103733.png|400]]

$$
\sum\Delta V = 0
$$
$$
\implies+V_{0} - \frac{q}{C}-iR+0=0 
$$
$$
\implies iR + \frac{q}{C} = V_{0} = \frac{dq}{dt}+\frac{1}{RC}q
 = \frac{V_{0}}{R}$$


$$
\frac{dq}{dt} = \frac{V_{0}}{R} - \frac{q}{RC} = \frac{CV_{0}-q}{RC}
$$
$$
\int_{0}^{q(t)} \frac{dq'}{CV_{0}-q}  = \int _{0}^{t} \frac{1}{RC}dt'  
$$
$$
q(t) = CV_{0}(1-e^{-t/RC} )
$$
([[Laplace transform]], [[Steady State Response]])