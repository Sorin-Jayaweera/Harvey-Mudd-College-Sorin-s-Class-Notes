
## Big takeaways



Potential temperature. 
$$
\begin{align}
\Theta \equiv  T \left( \frac{P_{0}}{P} \right)^{k}
\end{align}
$$

--- 


## Dry convection

We are thinking about parcel stability. 

Incompressible fluids have $T_{p}=T_{1}$ - the temperature is constant with height. If we have a compressible fluid, instead we need the dry adiabatic lapse rate $\Gamma_{d}$

$$
\begin{align}
T_{p} = T - \Gamma_{z} \Delta z
\end{align}
$$
The reference temperature decreases as we go up, since we are decreasing pressure. The stability actually needs to be relative to this reference point. 


The dry adiabatic lapse rate is commonly about $-10 \frac{K}{km}$.

--- 
### Potential Temperature

We know that $P=\rho RT$ (aka $PV=NRT$).

The first law of thermodynamics,
$$
\begin{align}
\delta Q = \delta W + \Delta V
\end{align}
$$

With the adiabatic assumption, we set 
$$
\begin{align}
0 = c_{p} dT - \frac{RT}{P}dp \\
\frac{dT}{T} = \frac{R}{c_{p} p}dp
\end{align}
$$
Lets define $\kappa\equiv \frac{R_{a}}{c_{p}}$.

$$
\begin{align}
\int \frac{dT}{T} = k \int \frac{dp}{p} \\
\ln (T) = K \ln (P) \\
\ln (T)- \ln (P^{k})= C \\
\ln \left( \frac{T}{P^{k}} \right)=c \\
\frac{T}{P^{k}}=C
\end{align}
$$


We define the Potential temperature (with units temperature) which is a reference to get around the temperature decrease from adiabatic expansion.

$$
\begin{align}
\Theta \equiv  T \left( \frac{P_{0}}{P} \right)^{k}
\end{align}
$$

## Moist convection


The adiabatic expansion isn't that accurate, because we have moisture. 

Latent heat: 
heat in the environment

Vapor Pressure - the partial pressure of water vapor

$$
\begin{align}
e = \rho_{v} R_{v} T = \frac{n_{v} }{n_{d}+n_{v}  }P
\end{align}
$$


Specific humidity: Mass of water vapour to mass of air
$$
\begin{align}
q = \frac{\rho_{v} }{\rho_{v} + \rho_{d} }
\end{align}
$$

Saturation specific humidity
$$
\begin{align}
q_{*}  = \frac{\frac{e_{s}}{R_{v} T} }{\frac{P}{(R_{a} T)}} = \frac{R_{a} }{R_{v} } \frac{e_{s} }{P}
\end{align}
$$


We define the relative humidity
$$
\begin{align}
U = \frac{q}{a_{*} }
\end{align}
$$


## Clausius - Clapeyron relation

$$
\begin{align}
\frac{d e_{s} }{dT} = \frac{L e_{s} }{R_{v} T^{2}}
\end{align}
$$
where $L$ is the latent heat with condensation / evaporation.  



Heat exchange is driven by phase changes.

We want
$$
\begin{align}
0 = c_{p} dT - \frac{1}{\rho} dp = L dq \\
0 = d \underbrace{ (c_{p}T + gz + Lq ) }_{ \text{ moise static energy } }
\end{align}
$$

If a parcel is saturated,
$$
\begin{align}
q^{*} = f(p_{1}T)
\end{align}
$$

$$
\begin{align}
dq^{*} = \left( \frac{ \partial q^{*} }{ \partial T } dT  \right) + \left(  \frac{ \partial q^{*} }{ \partial P }  \right)dP \\
\frac{ \partial q^{*} }{ \partial P } = \left( \frac{R_{a}}{R_{v} }  \right) \left(  \frac{-1}{p^{2}} \right)e_{s} = - \frac{q^{*}}{p} \\
\frac{ \partial q^{*} }{ \partial T } = \left( \frac{R_{a}}{R_{v} }  \right) \left( \frac{1}{p} \right) \frac{ \partial e_{s}  }{ \partial T } = \frac{R_{a} }{R^{2}_{v} } \frac{L}{R_{v} T^{2}} q^{*} 
\end{align}
$$

Remember that
$$
\begin{align}
q^{*} = \left( \frac{Ra}{R_{v} } \right) \frac{\underbrace{ e_{s} }_{ e_{s}(t)  } }{p}
\end{align}
$$

$$
\begin{align}
\frac{ \partial e_{s}  }{ \partial T } = \frac{L}{R_{v} } \frac{e_{s} }{T^{2}}
\end{align}
$$

We can now write out more directly the heat change driven by phase changes (phase change of water)

$$
\begin{align}
0 = c_{p} dT - \frac{1}{\rho} dp + L dq^{*} \\
0 = c_{p} dT + \frac{L^{2}}{R_{v} } \frac{q^{*}}{T^{2} }dT - \frac{1}{\rho}dp - \frac{Lq^{*}}{p}dp \\
0 = \left[ c_{p} + \frac{L^{2} q^{*}}{R_{v}T^{2} }  \right]dT + g dz \left[ 1+ \frac{L q^{*} \rho}{P} \right]
\end{align}
$$

We can rearrange to get
$$
\begin{align}
-\frac{dT}{dz} = \underbrace{ \frac{g}{c_{p} } }_{ \Gamma_{d}  }\underbrace{  \frac{[1+ L q^{*} / (R_{a}T) ]}{[1+ L^{2} q^{*}/(R_{v} T^{2})]} }_{ A }
\end{align}
$$
This $-\Gamma_{d}A$ is the saturated adiabatic lapse rate. 

We want to compare the temperature gradient with this saturated lapse rate to find stability. 


![[Pasted image 20260923141548.png]]
