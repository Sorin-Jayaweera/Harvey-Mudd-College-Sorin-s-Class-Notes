## Practical Questions

1) cost of sma
	1) 18-24 for regular looking (digikey)
	2) ~40 for fancier (mcmaster carr)

2) mating plane
	1) horizontal or vertical mating, how it takes up space on a pcb / mount
3) SMA insulation
	1) ![[Pasted image 20260831125411.png]]
	2) not sure what the "shield" is referring to - there is electrical insulation (PTFE) to reduce noise from external RF signals that aren't traveling along the signal's metal bit. The rest of the cable bits seem to either be for strength or electrical shielding. 
4) Field solver vs electrical simulator
	1) Field solver:
		1) Maxwell's equations from first principles
	2) Electrical Simulator
		1) using assumptions, just modeling current / voltage / capacitance / inductance using rules and abstractions from electromagnetic field - i.e higher order quantities using the various equivalents of ohms law (i.e. impedence versions for inductance and capacitance?) and differential equations. 
5) What assumptions foes LtSpice make during a DC simulation? Do capacitors matter?
	1) Ltspice uses currents - for no dynamics capacitors are opened circuits and capacitors are shorted. (stack exchange). 
6) What assumptions does LtSpice make during an ac simulation?
	1) uses complex node voltages, linearizing all nonlinear devices.
7) What assumptions does LtSpice make during a transient simulation?
	1) Waveform compression - Tstep is not useful
8) 3 ways to damage RF equipment
	1) not following power ratings (always look at dBm!)
	2) DC (always ac couple through a capacitor and use low voltages to not spark across the airgap)
	3) physically breaking stuff (don't bend wire bc reflections are bad)
## Theory Questions

1) What is the power dissipated in a 50 Ohm resistor (which is what most of our instruments look like) if it is driven by each of the following voltages? Express answers in both mW and dBm.

$$
\begin{align}
P = i^{2}R = \frac{V^{2}}{R}
\end{align}
$$

#### a.
1Vpp sinusoid with 0VDC offset

where $R$ is the resistance, the average power for a cycle is 
$$
\begin{align}
\frac{1}{2\pi R}\int_{0}^{2\pi} \sin(t)^{2} dt
\end{align}
$$
(dividing by $2\pi$ because we want the average power dissipation)
$$
\begin{align}
= \frac{1}{2\pi R} \int_{0}^{2\pi} \frac{1-\cos(2t)}{2}dt \\
= \frac{1}{4\pi R} \left(  t+\sin(2t) \right)\bigg|_{0}^{2\pi} \\
= \frac{1}{2 R}  
\end{align}
$$

At 50 Ohms, this is 
$$
\begin{align}
\frac{1}{100} = 10^{-2} \text{ W } \\
 & = 10mW
\end{align}
$$

in DMB this is
$$
\begin{align}
10 \, log_{10} \left( 10\right)   \\
= 10 \text{ dBm }
\end{align}
$$

#### b.
a 1Vpp sinusoid with 1VDC offset
Extrapolating from A:
$$
\begin{align}

= \frac{1}{4\pi R} \left(  3t+\sin(2t) \right)\bigg|_{0}^{2\pi} \\
= \frac{3}{2 R}  
\end{align}
$$


Watts:
0.03 W = 3 mW

dBm:

$$
\begin{align}
10 log_{10}(3) = 4.7 \, dBm
\end{align}
$$

#### c 
a 1Vpp square wave with 0VDC offset

Assuming this goes from -0.5 V to 0.5V the average power is
$$
\begin{align}
\frac{0.5^{2}}{R} = \frac{1}{4R}
\end{align}
$$


### 2:
Imagine 0dBm power is being dissipated in a load. First, express the load power in mW. Second, express the power level in dBm if the load power were multiplied by the following factors: 2x, 4x, 8x, 0.5x, 10x, 100x, 200x, 0.1x. Logarithmic math is your friend here, and this problem may go faster if you look for additive patterns in the results.

We know that
$$
\begin{align}
0 dBm = 1 mW. \\
\end{align}
$$
For each of the factors (n) we have
$$
\begin{align}
10log_{10}(n)
\end{align}
$$
With logarithms we have the product rule, and can just do this easily (i.e. log10(4) = log10(2) + log10(2))

We're just adding the logs of the factors (2 and 10 matter). 

| Multiplier/Power (mW) | Power (dbm) |
| --------------------- | ----------- |
| 1                     | 0           |
| 2                     | 3.          |
| 4                     | 6           |
| 8                     | 9           |
| 0.5                   | -3          |
| 10                    | 10          |
| 100                   | 20          |
| 200                   | 23          |
| 0.1                   | -10         |

# Lab

Circuit:
![[Pasted image 20260901083154.png|300]]

### DC Operating point simulation:

![[Pasted image 20260901083140.png|300]]


### DC sweep of R2 (resistor connected to output and ground)
current:
![[Pasted image 20260901190704.png|300]]
voltage:
![[Pasted image 20260901191644.png|300]]
vs desmos for a voltage divider
$V_{\text{ out }}=\frac{R_{2}}{R_{1}+R_{2}}V_{\text{ in }}$

![[Pasted image 20260901191326.png|500]]
These look the same!

### AC sweep around the corner frequency
![[Pasted image 20260901192953.png]]

The corner frequency appears to be around 24 hz. 

We can calculate this by writing out the impedence of each source, and finding the transfer function (which took way too long from dumb algebra errors):
![[Pasted image 20260903203506.png]]

We have
$$
\begin{align}
V_{\text{ out }} = Vin\left( 1- \frac{R_{1}}{R_{1}+ \frac{1}{\frac{1}{R_{2}}+cs}} \right) \\
H = 1- \frac{\frac{R_{1}}{R_{2}}+R_{1}cs}{\frac{R_{1}}{R_{2}}+R_{1}cs+1} \\
= 1 - \frac{\frac{R_{1}}{R_{2}}+R_{1}cs}{R_{1}CS+ \left( \frac{R_{1}}{R_{2}}+1 \right)} \\
1- \frac{1}{\left( \frac{R_{1}}{R_{2}}+1 \right)}\frac{\text{ don't care }}{\frac{R_{1}CS}{\frac{R_{1}}{R_{2}}+1}+1}
\end{align}
$$
(we don't care about the top for now - although because it has an S, I think this has a second corner frequency at half power? Its not second order because its not $S^{2}$, its a zero instead of a pole. IDK, i didn't take E102).
We know that we have 
$\frac{S}{\omega}$, so we get

$$
\begin{align}
2\pi f = \frac{\frac{R_{1}}{R_{2}}+1}{R_{1}c} \\
f = \frac{\frac{R_{1}}{R_{2}}+1}{2\pi R_{1}c} \\
= 23.8 hz
\end{align}
$$
This agrees closely with what we found in the simulation (with large error from my arbitrary mouse position)

Full workthough on a whiteboard:
![[Pasted image 20260904173549.png]]
(I realized after I took the photo that I dropped a $(1+CSR_{2})$ in the numerator)

$$
\begin{align}
H(s) = \frac{R_{1}(R_{1}+R_{2})(1+CSR_{2})}{\frac{R_{1}R_{2}CS}{R_{1}+R_{2}}+1}
\end{align}
$$

### Transient of a step input in voltage

![[Pasted image 20260901193239.png]]

Because $\tau = \frac{1}{\omega_{c}}$, $= \tau\frac{1}{24*2\pi}=0.0067=6.7ms$

The actual one (in the simulation) is ~ $666*(1-e^{-1})=421mv$, which happens at $6.7~ms$ ish. This is great!

--- 
EXTRA WORK BC I'M A DUMBASS AND FORGOT that $\tau = \frac{1}{\omega_{c}} s$ (and so derived it from scratch... I love being a physicist). 
Because we have the transfer function from before $H(s)$, we can get the rise time. We multiply the transfer functions of a step function $G(s)$ and our $H(s)$ to get the response to that step. 

$C(s)=G(s)H(s)$

$R(s)=\frac{1}{s}$
So we have 
$$
\begin{align}
\frac{1}{s}\frac{R_{1}(R_{1}+R_{2})(1+CsR_{2})}{\frac{R_{1}R_{2}CS}{R_{1}+R_{2}}+1}
\end{align}
$$
Lets call
$\frac{R_{1}R_{2}C}{R_{1}+R_{2}}=\frac{1}{\omega_{c}}$

this becomes
$$
\begin{align}
\frac{R_{1}(R_{1}+R_{2})(1+Cs R_{2})}{\frac{s^{2}}{\omega_{c} }+s} \\
=\frac{R_{1}(R_{1}+R_{2})(1+Cs R_{2})}{s(\frac{s}{\omega_{c} }+1)}

\end{align}
$$


We can separate this with partial fractions

$$
\begin{align}
\frac{A}{S}+ \frac{B}{\frac{s}{\omega_{c} }+1} \\
\end{align}
$$

$$
\begin{align}
\frac{As}{\omega_{c} }+Bs  & = CsR_{2}(R_{1}^{2}+R_{1}R_{2}) \\
A & = R_{1}(R_{1}+R_{2})
\end{align}
$$
We can solve
$$
\begin{align}
\frac{R_{1}(R_{1}+R_{2})^{2}}{R_{1}R_{2}C}+Bs= CsR_{2}(R_{1}^{2}+R_{1}R_{2}) \\
B = \frac{R_{1}R_{2}^{2}C^{2}(R_{1}^{2}+R_{1}R_{2})}{R_{1}(R_{1}+R_{2})^{2}}
\end{align}
$$
Lets leave those as constants $A$ and $B$ because they're nasty AF. We can plug in numbers later. 

$$
\begin{align}
C(s)  & = \frac{A}{s} + \frac{B}{\frac{s}{\omega c} + 1}   \\
 & = \frac{A}{s}+ \frac{B\omega_{c}}{s+\omega_{c} } 
\end{align}
$$


This gets us
$$
\begin{align}
c(t) = A + B\omega_{c}e^{-\omega_{c}t } 
\end{align}
$$


This is where I remembered, at the end, that $\omega c=\frac{1}{\tau}$. QED.

--- 


## S Parameters

$S_{11}$ is always at $0$dB, so I am not inclined to trust this. However, this is what I'm getting for following the tutorial found here:
https://www.designers-guide.org/forum/Attachments/CreateS-ParameterSUBCKTinPSpice.pdf

![[Pasted image 20260904185701.png]]

With 1 V DC on every voltage source (not sure why this should matter, but it does). Note different axis labels because behavior changed starkly (f=10k vs 100k). 
![[Pasted image 20260904191049.png]]