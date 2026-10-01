
In this lab you are going to simulate reflections on transmission lines to predict the types of voltages you would see at drivers, loads and selected points in the middle of a transmission line.

After this lab, you will be able to:

1. Calculate reflection coefficients and voltage distributions on transmission lines.
2. Predict the time scales and shapes of reflection events at the driving point and load of a transmission line
3. Simulate voltages produced at the terminals of a lossless transmission line.
4. Measure transmission line transients in the lab and understand practical features of lab equipment that affect those transients.
5. Understand, visualize and calculate standing wave patterns on a transmission line.
6. Calculate the load impedance that would generate a measured reflection.

## Theory Questions

1. RF cables and some connectors for RF systems are described by their “electrical length.” What is electrical length? Imagine that you used a connector to attach BNC cables to an oscilloscope, how would you measure the electrical length of the connector if you were uncertain of the velocity in the cables? (You may search on the internet to find the answer to this question. Just understand what you find and answer in your own words.)


The number of wavelengths / full rotations of a frequency that fit along the length of the cable. It is more useful to think in terms of the wavelength / frequency as a reference so that we have a standard measurement across frequency ranges.


For the following questions, note that BNC cables are transmission lines that have a velocity factor of 0.66 and a characteristic impedance of 50 ohms. Note also that function generators almost all have 50 ohms of source impedance.

2. Consider an oscilloscope and function generator connected as shown in Figure 1 (the box in the figure represents two separate instruments). Calculate the voltage waveforms you expect to see at channels 1, 2 and 3 after Gen Out drives a 1V step onto the transmission line for the terminations listed below. You must deliver a waveform for channels 1, 2 and 3 (possibly overlaid on one another, as if you had measured them on an oscilloscope) as an answer for each scenario.  
      
    Note: This is a lot of math. You may be able to save yourself time with code and/or AI tools. You can generate the plots however you want and you do not have to use AI, but you may be able to save time by writing out what the waveforms should look like, and then asking an AI chatbot to generate the figures for you. You may have even better luck asking an AI chatbot to write code to generate the figures. To be clear, you may NOT use AI to directly calculate or generate code that calculates what the waveforms should be—but you may do the calculations yourself (by hand or writing your own code), then use AI to write code that purely generates plots of the shape you specified. You will still be responsible for the accuracy of your figures (you have to make sure the AI tool correctly interprets what you give it). Up to you! But the intent of this exercise is to learn about time delay and reflections, not spending a long time drawing.



![[Pasted image 20260911175527.png]]


The voltage wave would travel through each connection until the end, where it would reflect back. The total length of wire is roughly 30 feet. at 0.66 feet per nanosecond, from the start of the rise at the 12 ' BNC to the start of the 18' BNC, there would be $\frac{12ft}{0.66 \frac{ft}{ns}}= 18ns$. To the end of the 18' BNC the step would take $\frac{30ft}{0.66 \frac{ft}{ns}}=~45$ ns (27 ns for that step). It would take the same time steps for the reflected wave to travel backwards.

2. An open circuit

The open circuit has a reflection coefficient $+1$. After the wave hits the end (45 ns = 63 ns) we would see double the voltage as the wave travels back. 

*Claude plot*
![[Pasted image 20260912144732.png]]


LT SPICE
![[Pasted image 20260912160717.png]]


Experiment
![[PNG9999 1.png]]


These look the same qualitatively, with noise and slight time differences since the real wires are not exact lengths! The spike turns on around 45 ns, the first cable sees a rise roughly 28 ns after that, and the third rises roughly 30 ns after that. 

At 0.66 ft/ns, the first length is roughly  


3. 50 ohms.

We have the reflection coefficient while the wave is traveling (it looks like a voltage divider).

This gives us
$\frac{50-50}{50+50} = 0$. No voltage will reflect, so it'll just look like the 1 v step with some delay. 

![[Pasted image 20260912145134.png]]



LT SPICE plot
![[Pasted image 20260912160344.png]]

Experiment
![[PNG50 1.png]]
4. A short circuit
Short circuits have reflection coefficients of -1, so that the reflected wave cancels out the forward one after it bounces off the end. It travels the whole way, tying the function generator straight to ground (assuming now that the function generate is an infinite current source? It is either 1 volt or 0 volts depending on the behavior of the generator. )


![[Pasted image 20260919095143.png]]

![[Pasted image 20260912160815.png]]


Experiment:
![[Senior/RF/labs/lab 2/images/PNG0.png]]

5. 22 ohms

$$
\begin{align}
\Gamma = \frac{22-50}{50+22} = -\frac{28}{72}
\end{align}
$$
This means that -0.39 volts would reflect back, so 1-0.39 volts ~= 0.6. would be seen at the termination, which would travel backwards. 

*Claude Plot*
![[Pasted image 20260912150014.png]]

![[Pasted image 20260912150151.png]]


LT SPICE:
![[Pasted image 20260912160851.png]]

Experiment:
![[PNG21.png]]

6. 200 ohms

$$
\begin{align}
\Gamma= \frac{200-50}{50+200} = \frac{150}{250}
\end{align}
$$

![[Pasted image 20260912150132.png]]
![[Pasted image 20260912150153.png]]


LT SPICE (perfect):

![[Pasted image 20260912160925.png]]


Experiment:
![[Senior/RF/labs/lab 2/images/PNG200.png]]

This looks closer to my prediction than the LT spice simulation!





## 3

1. Consider an oscilloscope and function generator connected as shown in Figure 2. Calculate the voltage waveforms you expect to see at oscilloscope channels 1, 2 and 3 after gen out drives a 1V step onto the line for the values of shunt and termination resistors listed below. You must deliver a drawn waveform for channels 1, 2 and 3 (possibly overlaid on one another) as an answer for each scenario.

2. 50 ohm shunt and 50 ohm termination 🡨 hint: think about energy conservation
With both of them at 50 ohms we don't have any reflection. At the split for the shunt and the 18 foot BNC, the cables both look equivalent so the voltage wave travels at half power on both paths. Therefore, we would have $\frac{1}{\sqrt[]{ 2 }}V$  at the 18' BNC end of the line (the last node). The voltages before the resistors are held at 1 from the source, and the voltages.


*Claude Plot*
![[Pasted image 20260912151335.png]]


*Side note*: Claude said that the termination and shunt should be shown in parallel (which I had the thought of before the output and had verbalized it, but hadn't written it out first. ERGO I'm ignoring that even though I agree that it should be treated as parallel. I also want to build intuition for how this would work if there are no reflections at perfect terminations. I could probably think in terms of currents, but idk). 


LT SPICE:

![[Pasted image 20260912161724.png]]

This looks really different from what I had thought it would. We have 0 volts at note B but some voltage at node C? 


Experiment:![[PNG5050.png]]


3. 50 ohm shunt and 200 ohm termination 🡨 don’t solve this exactly because it’s a longwinded pain, a general discussion of what happens at the first few reflections and the point to which the line voltage converges is OK.

Equal voltages go down each path initially ($0.707 V$ because half power). 

- At the 50 ohm shunt there will not be a reflection. The voltage wave will finally reach the termination and become a voltage divider as time $\to \infty$. 

- Before interacting, the half power wave goes down the 18' BNC. 
- At the termination, we'll have a reflection coefficient $\frac{150}{250}$, so a positive voltage wave will bounce back and add to the voltage across the 18' bnc. 
	- This voltage wave will go through both the shunt and up the 12' bnc path (at half power, so $\frac{1}{\sqrt[]{ 2 }}* \frac{15}{25}$) additional voltage. One side will go down through the 12' bnc and the gen out, and the other half will go to the shunt where it will go to ground. The voltage at the shunt will equal the voltage on the 18' cable. As a voltage divider in steady state, the voltage at the 18' bnc becomes
$$
\begin{align}
\frac{200}{250} V
\end{align}
$$

We didn't have to solve exactly, so I didn't make a plot.

LT SPICE:

![[Pasted image 20260913102747.png]]


![[PNG50200.png]]

4. Short shunt and open termination
We are grounding the 18' BNC, so no voltage would go there (assuming the shunt has 0 length and is immediately grounded, no voltage wave would 'escape' to the rest of the line). 

The wave travels until it splits to half power (0.7 V) at the junction. At the ground side, a negative wave goes backwards and splits up to the fxn generator, and to the open termination. The open termination original wave will bounce back and double the voltage, which will travel back until the negative wave drops it again. We'll see a little blip. 



![[Pasted image 20260913102850.png]]

![[PNGNB 3.png]]



![[Pasted image 20260911175629.png]]


## 4
1. Finally, consider an oscilloscope and function generator connected as shown in Figure 3. Assume the termination is a 22-ohm resistor and the generator is driving a sinusoid.

2. What VSWR do you expect on the transmission line?

$$
\begin{align}
VSWR = \frac{ 1 +\left|\Gamma \right| }{ 1-\left|\Gamma \right| }
\end{align}
$$

where $\Gamma= -\frac{28}{72}$


So we have
$$
\begin{align}
VSWR = 2.27
\end{align}
$$



1. If you wanted to sweep the frequency of the input sinusoid to observe the maxima and minima of a standing wave at channel 2, what frequency would you start at and what frequency would you end at? Note this function generator maxes out at 20Mhz.

$$
\begin{align}
f_{1}=\frac{\left( \frac{f_{0}}{0.66c} [\frac{\text{ cycles }}{m}] * 14.6304 [m]*2[ \frac{\text{ cycles standing }}{\text{ cycles reg }}] + 0.25[ \text{ cycles } ]\right)}{14.63 [m]} * 0.66 c
\end{align}
$$
It's 0.25 cycles, because half a cycle would go from a null to a null, so 0.25 is from null to peak. 

For $f_{0}= 10^{6}$ Hz, this would make $f_{1}=5383366.14$ Hz



2. Provide a sketch of the expected amplitude of the sinusoidal voltage at channel 2 vs. frequency for the frequencies between the values you found in part b.

![[Pasted image 20260918164029.png]]


![[Pasted image 20260911175700.png]]




## Lab Instructions

1. Use **lossless** transmission line elements to simulate the scenarios that you calculated waveforms for in the theory section. Compare your simulation and calculations.
2. Build these scenarios from the theory section in the RF lab and record measured voltages at the oscilloscope terminals. Compare your simulation, calculations and theory.


# Experimental section

## LTSPICE Simulation


I'm putting the LTSPICE simulation plots next to the other plot to make comparison easier


## Lab 

### Circuit 1:

![[Pasted image 20260912134038.png]]

![[20260912_134220.jpg|2000]]


### Circuit 2:


![[Pasted image 20260911175629.png]]

I forgot to get a photo of the setup, its basically the same but with a splitter and another termination added.


### Circuit 3

![[Pasted image 20260911175700.png]]


We start at 1 Mhz. We set the function generator to output the sync squrae wave, which we trigger on to. We sweep frequencies to find where there is a $\frac{\pi}{2}$ phase shift. 

The zero happens at $7.6 MHz$, and again at 13.5 Mhz, and finally at ~ 21 Mhz. . 

![[20260922_201220.jpg]]
![[20260922_201209.jpg]]
![[20260922_201100.jpg]]




### Mystery Load
2. In the lab, you will find a “mystery load” (Figure 4). Use your test setup from the previous problems to measure the reflection of the mystery load (e.g., use it as the termination in Figure 1). You don’t need to use the exact test setups from the previous portions of the lab; you just need to be able to calculate the reflection off of this load from your measurements. Calculate the reflection, then determine the impedance that would give you that reflection. Finally, determine the circuit that gives you that impedance (it’s two components).



![[PNGNB 1.png]]

This tells us the reflection coefficient - also the final voltage is higher, so additive (aka positive $\Gamma$). 
X


If we apply a step function, we see the initial voltage (622 mV) step up by 100mV to 722 mV.  This tells us the magnitude of the reflection coefficient  is

$$
\begin{align}
\Gamma & = \frac{100}{622} = \frac{Z-50 }{Z+50} \\
\Gamma(50+Z) & = (Z-50) \\
50\Gamma+ Z \Gamma + 50  & =  Z \\
(50 \Gamma+ 50)  & = Z (1-\Gamma) \\ \\
Z  & = 50\frac{(\Gamma+1)}{\Gamma- 1} \\
 & \approx 69 \Omega
\end{align}
$$

Because we have to elements in parallel, $69 \Omega$ is the parallel impedance of both elements. We would have an open circuit if the capacitor were in series (?) because long term this should look like DC, so its has to be in parallel.

For a parallel RC circuit, 
$$
\begin{align}
z = \frac{RC}{\sqrt[]{ R^{2}+C^{2} } }
\end{align}
$$



We found 17 MHz to be roughly the corner frequency (very roughly) because of a 90 degree phase shift. 


![[PNGMPH.png]]

We found the corner frequency, and slightly decreased frequency. The wave moved to the right, meaning that it has a negative phase (it is lagging behind the signal) - ergo, it is a capacitor.  We can use the corner frequency to find the capacitance. 

![[PNGCAP.png]]
In this figure, we slightly decreased the frequency and determined that we had a capacitor and not an inductor. 

# TODO: This is in parallel not series

For an RC circuit, the corner frequency is
$$
\begin{align}
f_{c} = \frac{1}{2\pi RC}
\end{align}
$$



We now have two equations:


$$
\begin{align}
f_{c}  = \frac{1}{2\pi RC} \\
\omega = \frac{17*10^{6}}{2\pi} \left[ \frac{\text{ rad }}{\sec} \right]
\end{align}
$$
and
$$
\begin{align}
\frac{1}{\frac{1}{R_{1}}+\frac{1}{Cs}}= 50
\end{align}
$$








![[Pasted image 20260911175722.png]]



1. Here are a bunch of useful hints:

2. Don’t forget about the “out-term” setting on function generators. It should be set to Hi-Z. If it is set to “50 Ohm”, then your measurements will appear to be off by a factor of 2.
3. When you make a resistive or short termination, don’t put it at the end of another length of transmission line. (For reasons we’ll go over soon, that will mess up your measurement.) Use BNC tee connectors and BNC-banana connectors to create a short/resistor that attaches right onto the oscilloscope channel..
4. The expectation in this class is that you can make simulations, calculations and theory match well, and that any deviations between them are **_quantitatively_** explained. (e.g., “the connector is 1cm long and velocity in it is different than the transmission line, which accounts for the extra 2cm of length extracted from the waveform” is better than “these don’t match because we didn’t account for the connectors.”)
5. Achieving these quantitative descriptions may require you to perform a process called parasitic extraction, where you add parasitic elements to your simulation and adjust them until it matches your measurements. A little parasitic inductance (approx. nH) in series with grounded elements is often all you need. This is especially important for short terminations. You may also need to adjust the lengths of the transmission lines in your simulation to agree with your measurements, as the cable lengths are inaccurate by a few inches.
6. You will need to include loss in your simulated transmission line models for the scenario in Figure 3. These links will help:  
    [http://ltwiki.org/index.php?title=O_Lossy_Transmission_Line](http://ltwiki.org/index.php?title=O_Lossy_Transmission_Line)  
    [https://electronics.stackexchange.com/questions/323647/ltspice-how-to-model-a-tline](https://electronics.stackexchange.com/questions/323647/ltspice-how-to-model-a-tline)
7. We have a rig to help you build out your BNC measurements, thanks E4 students! See below. This rig cleans up your measurements a lot by reducing strain on the connectors. It’s already set up with the cable lengths you need! Don’t disconnect the wrapped up cables in the back! If you do, you get to grab a tape measure and lay a bunch of cables out in the hallway outside the RF lab at night, then measure out the right lengths of cables to rebuild the rig, which is exactly what Prof. Donahue did this summer before classes started!)

![[Pasted image 20260911175740.png]]


