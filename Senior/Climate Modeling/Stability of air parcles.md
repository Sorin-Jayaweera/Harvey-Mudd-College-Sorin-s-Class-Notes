
>[!abstract]+ Key Points
>the first law of thermodynamics states that the internal energy of a system - the work done by a system is the change in temperature of the system
>
>If a parcel of air is raised adiabatically, the temperature of the parcel will decrease as it expands.
>
>If the temperature of the parcle of air changes, it hasn't necessarily exchanged heat with its surroundings.
>
>The adiabatic lapse rate is the change in temperature of the environment due to adiabatic expansion
>
>The atmosphere is not unstable to dry convection.
>
>Potential temperature is a useful reference because it is constant, and tells us stability better. 

If denser air is on the bottom, it is stable. If denser air is up, it is negatively buoyant and will fall - an unstable system. The Troposphere -> stratosphere has a temperature inversion, where the troposphere is unstable (warmer air lower).

We have a system that is more complicated than just a temperature gradiant causing convection. Air is compressable

Imagine a piston lowered on a vessle of air, pushing down on a column by $dh$. The surroundings have done work on the system.

$$
\begin{align}
\delta W = \Sigma \text{ work } = \Sigma \text{ force x displacement } \\
= pA dh (\text{ Pressure * Surface Area* displacement}) \\
= P \underbrace{ dV }_{ \text{ volume } }
\end{align}
$$
$$
\begin{align}
W = \int_{\text{ initial }}^{\text{ final }} P dV
\end{align}
$$

This is Pressure-Volume work. 

If no heat is exchanged, the change in internal energy is just the work done (adiabatic). 

$$
\begin{align}
\underbrace{ U_{final}  }_{\text{ energy}} = U_{\text{ initial }} - W
\end{align}
$$
Note that $w>0$ when the gas does work on the environment. 


First law of thermodynamics
$$
\begin{align}
\Delta U + W = Q
\end{align}
$$
The change of energy to a system + the work done by the system = net heat. 


## Compressible Fluids

How does the density $\rho$ (and $t$) change in response to a perturbation.


$$
\begin{align}
PV=nRT
\end{align}
$$
where $R$ is the ideal gas constant

$$
\begin{align}
\rho = \frac{m}{V} = \frac{n_{a} m_{a} }{V}
\end{align}
$$

$$
\begin{align}
P = \frac{\rho}{m_{a} }RT
\end{align}
$$
because $\frac{\rho}{m_{a}}=n$. We can move the $m_{a}$ constant, and get

$$
\boxed{
\begin{align}
P=\rho R_{a} T
\end{align}
}
$$
where $R_{a}= \frac{R}{m_{a}}$ is the air specific gas constant. 

We are not conserving parcel temperature - the parcels cool as they expand. We are also letting the parcel expand as it goes up, doing work on the environment (and decreasing density) which will cool it down. 

## Dry Air expansion

First law of thermodynamics
$$
\begin{align}
dU + \delta W = \delta Q \\
dU + PdV = \delta Q
\end{align}
$$

We define thermal capacity
$$
\begin{align}
C \equiv \frac{ \partial Q }{ \partial T } 
\end{align}
$$
the amount of heat absorbed by the body per change in temperature.

At constant volume $dV = 0$, so the heat capacity at a constant volume is
$$
\begin{align}
C_{V} \equiv  \left( \frac{\partial Q}{\partial T} \right) = \left( \frac{ \partial U }{ \partial T }  \right)_{V} 
\end{align}
$$

If we have a constant volume, we have

For an ideal gas $U=U(T)$ so we don't have to assume constant volume. 
$$
\begin{align}
C_{V} = \frac{\partial U}{\partial T}
\end{align}
$$
$$
\begin{align}
c_{v} dT + P dV = \delta Q \\
\rho V = 1
\end{align}
$$


$$
\begin{align}
V  & = \frac{1}{\rho} \\
dV  & = d\left(  \frac{1}{\rho} \right) \\
 & = -\frac{1}{\rho^{2}}d\rho
\end{align}
$$

$$
\begin{align}
P dV = \frac{-p}{\rho^{2}}d\rho
\end{align}
$$
With the ideal gas law, 
$$
\begin{align}
P = \rho R_{a} T \\
dP = R_{a} T d\rho + \rho R_{a }dT \\ 
\end{align}
$$
$$
\boxed{
\begin{align}

d\rho = \frac{1}{R_{a} T}d\rho - \frac{\rho}{T}dT
\end{align}
}
$$
We can substitute that back in to our dry air expansion bit

$$
\begin{align}
P dV  & = \frac{-P}{\rho^{2}} d\rho \\ \\
P dV  & = -\frac{P}{\rho^{2}}\left( \frac{1}{R_{a} T}d\rho - \frac{\rho}{T}dT \right) \\
P dV & = \frac{-P}{\rho^{2}R_{a} T} d\rho + \frac{P}{\rho T}dT \\
P dV  & =  \frac{-1}{\rho}dp + RdT \\
\end{align}
$$

$$
\begin{align}
c_{v} dT + \rho dV  & = \delta Q \\
(C_{v} +R)dT - \frac{1}{\rho} dp  & = \delta Q \\
c_{p}  & = c_{v} +R
\end{align}
$$

## Hydrostatic balance
$$
\begin{align}
-\rho g = \frac{ d p}{d z } 
\end{align}
$$


Lets take the derivative of our compressible fluid equation

$$
\begin{align}
c_{p} dT = \frac{1}{\rho}dP \\
\frac{dT}{dz} = \frac{-g}{c_{p} } = - \Gamma_{d} 
\end{align}
$$

where $\Gamma_{d}$ is the dry adiabatic lapse rate.



# Exersize

Temperature at two points:
lower = 289.625
higher = 256.376
that are separated by 5.196 km
$\Gamma_{d}$ = 10 $\frac{K}{km}$ (10 kelvin per kilometer). 

$$
\begin{align}
T_{p} = T_{1} - \Gamma_{d}  \Delta z 
\end{align}
$$

This gives us about 51.9 kelvin difference adiabatically. 

The actual temperature difference is 33 k.  (or 6.6 degrees per kilometer). 

For just expansion
$$
\begin{align}
T_{2} = T_{1} + \frac{ \partial T }{ \partial z } \\
 
\end{align}
$$

This system is still just stable. 


# As the air parcle rises it will expand and loose heat. For stability we don't care about only the number, but actually temperature relative to the temperature if the parcel were only subject to compression.



To correct for temperature changes so that we have a constant reference number, we define a new variable - the potential temperature. 

$$
\begin{align}
c_{p} dT = \frac{R_{a} T}{p}dp \\
\frac{ d T}{d T } = \frac{R_{a} }{c_{p} }\left( \frac{dp}{p} \right)
\end{align}
$$
where $k \equiv \frac{R_{a}}{c_{p}}$

$$
\begin{align}
\int \frac{dT}{T}= k \int \frac{dp}{p} \\
\ln (T) = k \ln  p + C \\
\ln T - \ln (P^{k})= C \\
\ln \left( \frac{T}{p^{k}}  \right)= c
\end{align}
$$

This is potential temperature

$\theta \equiv T \left( \frac{P_{0}}{P} \right)^{k}$

