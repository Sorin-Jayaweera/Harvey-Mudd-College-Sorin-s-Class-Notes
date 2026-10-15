
Designed for a source impedance and load impedance of 50Ω

• Pass band edge of 100MHz

• Stop band start of 200MHz

• 20dB of rejection in the stop band

• Insertion loss of less than 3dB

• In-band ripple of less than 1dB


|                                                         |             |                                                         |                                                           |                                            |                                                             |
| ------------------------------------------------------- | ----------- | ------------------------------------------------------- | --------------------------------------------------------- | ------------------------------------------ | ----------------------------------------------------------- |
| Parameter                                               | Analytical  | Simulated w/ ideal components                           | Simulated w/ real versions of Ideal components components | Simulated with final real component values | Measured                                                    |
| Filter type (Butterworth, Chebyshev I, etc.)            | Butterworth | NA                                                      | NA                                                        | NA                                         | NA                                                          |
| Filter order                                            | 5           | NA                                                      | NA                                                        | NA                                         | NA                                                          |
| Pass Band Edge<br><br>(defined as exceeding 1dB ripple) | 120MHz      | 104MHz                                                  | 103MHz                                                    | 144 MHz                                    | -1db happens at 135 MHz, but phase - 180 happens at 110 MHz |
| Stop Band Start  <br>(defined @20dB of rejection)       | 200MHz      | 165MHz                                                  | 163 MHz                                                   | 190 MHz                                    | 196 MHz (SO CLOSE AAAGH)                                    |
| Insertion Loss                                          | -3 dB       | -0.17dB (or 6.17 if we don't remove the expected -6 dB) | -0.106                                                    | -0.59                                      | -0.4                                                        |
| In-Band Ripple                                          | 1 dB        | 0.1 dB (what? crazy)                                    | 0.7 dB                                                    | 0.2 dB                                     | 0.7 dB                                                      |


## Deriving Analytically the filter values



Analytical:

The pass band ripple has to be less than $1dB$, so
$\delta=1$
$$
\begin{align}
\epsilon & =\sqrt[]{ 10^{0.1\delta}-1 } \\
  & = \sqrt[]{ 10^{0.1} -1} \\
 & \approx0.508 
\end{align}
$$
This is the maximum passband gain, aka the insertion loss. 

For a butterworth filter,
$$
\begin{align}
n = \frac{\ln \left( \frac{A_{s}}{\epsilon}  \right)}{\ln \left( \frac{\omega}{\omega_{p} } \right)}
\end{align}
$$

where $A_{s}$ is the stop band rejection, $\epsilon$ is this pass band parameter, $\omega$ is the stop band frequency, $\omega_{p}$ is the center of the pass band.

$$
\begin{align}
A_{\text{ stopband }} =-20dB=10^{\frac{20}{20}}=10 \\
\epsilon=0.508 \\
\omega_{p} =100MHz *2\pi\\
\omega=200MHz*2\pi 
\end{align}
$$

This gives us
$$
\begin{align}
N=4.299
\end{align}
$$
So we'll need a 5th order filter to hit these specs (4th order is barely too weak).

![[Pasted image 20261011141324.png]]
and R is just 50 Ohm.


![[Pasted image 20261011121015.png]]

For capacitors
$$
\begin{align}
\frac{c_{nor}}{\omega_{p} z_{0} }=c 
\end{align}
$$
For inductors
$$
\begin{align}
L=\frac{z_{0}L}{\omega_{p} }
\end{align}
$$

|                 |                  |     |                   |              |               |             |
| --------------- | ---------------- | --- | ----------------- | ------------ | ------------- | ----------- |
| Name            | Normalized Value | z0  | Component value   | OOM          | nano unit     | pico unit   |
| C1              | 0.618            | 50  | 0.00000000001967  | -10.7061614  | 0.01967155097 | 19.67155097 |
| L2              | 1.618            | 50  | 0.000000128756349 | -6.890231347 | 128.756349    | 128756.349  |
| C3              | 2                | 50  | 0.00000000006366  | -10.19611988 | 0.06366197724 | 63.66197724 |
| L4              | 1.618            | 50  | 0.000000128756349 | -6.890231347 | 128.756349    | 128756.349  |
| C5              | 0.618            | 50  | 0.00000000001967  | -10.7061614  | 0.01967155097 | 19.67155097 |
| frequency rad/s |                  |     |                   |              |               |             |
| 628,318,531     |                  |     |                   |              |               |             |
At first I did it with these component values, as it should theoretically work for 100MHz. However, in simulation it was not sufficient. I changed them to be centered at 120MHz, and it worked perfectly. 

![[Pasted image 20261011154856.png]]
(pasting values stopped working on my computer for some reason)

![[Pasted image 20261011154555.png]]

![[Pasted image 20261011154615.png]]

I see -6.3 dB at 100MHz, and -28 dB at 200 MHz. If we remove the 6 db garunteed attenuation, yippee!



## Simulation of Real component Values

The closest I could find in the lab were 100 nH, 15 pF, and 56 pF. 
![[Pasted image 20261011160052.png]]

![[Pasted image 20261011160101.png]]


When I measured these components, I saw $-2dB$ insertion loss, which (by playing with numbers in simulation) corresponds to about 10 $\Omega$ in series with the filter. 

S12 insertion loss of the chart of the circuit that I designed

![[PNGsorinorigional 1.png]]

S11 of that same circuit

![[PNGsorinorigionals11 1.png]]

Smith chart of that same circuit

![[PNGsorinorigionalsmith 1.png]]



After much pain (so many components, so much trying to shift the speed of the cutoff and the position of the cutoff left / right to get the < 1$db$ loss passband and the $>20$db loss stopband). I have it at 1.35 dB loss in the passband (so close!) and -21 dB loss in the stopband (really really close to the restriction!). I have also gotten it to 0.7 dB in the pass band, but -18 in the stopband, which felt worse because noise would be twice as strong. I, as a real engineer, would sacrifice 0.6 db to get 3 db better stopband. 

The component values are now: 100nH for both inductors (although i did try 150nH for a while), 20 pF for the first capactior, 33p for the second (middle), and 24pF for the last one. 

![[Pasted image 20261011191046.png]]![[Pasted image 20261011191059.png]]

Real data:
S11
![[PNGmehs11.png]]

S21
![[PNGmehs12.png]]

Butterworth was the wrong choice for this. I should have done a Chebyshev - I just really wanted to minimize ripple at the pass band. 


Smith
![[PNGmehsmith.png]]

Phase
![[PNGphase.png]]



In the tighter range around the pass band (log magnitude because it is nicer imo):
![[PNG1 1.png]]

Linear scale because you asked for it
![[PNG1 2.png]]




The simulation of the filter shows an expected -17dB(after subtracting 6) at 200 MHz, the corner at 132 MHz, and -1.3 dB at the input. This is extremely close (having added 10 $\Omega$ of series resistance). Given that the corner frequency is slightly different in the simulation and the real one, that tiny shift likely corresponds to the 3dB difference at 200 MHz. The peak would have to shift back a liiitle bit. By changing the center capacitor to 40p, we recreate nearly exactly what the curve looked like. This means that we had roughly 10pF of parasitic capacitance in parallel on some of the components. We could recreate the same thing if instead we had a little bit more inductance than advertised - raising the inductance pushes forward the corner frequency, which decreases the attenuation at 200 MHz.  


# TODO




three other things for tight range of pass band

Calculation showing power delivered to a 50 Ohm if your filter were driven by a 1Vpp, 0VDC offset, 50 MHz sine wave from a voltage source w/ 50 Ohm output impedance.  You will need your measured insertion loss to complete this calculation, and you may refer to the page in your report where I can check it.





# Random plots that I don't remember what they were from

![[PNGsorinorigional.png]]

![[PNGsorinorigionals11.png]]

![[PNGsorinorigionalsmith.png]]
