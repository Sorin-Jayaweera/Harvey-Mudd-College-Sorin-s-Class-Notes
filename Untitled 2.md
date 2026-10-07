
$$
\begin{align}
E(\alpha,\beta) = \frac{N(\alpha, \beta) + N(\alpha \perp, \beta \perp ) - N(\alpha, \beta \perp) - N(\alpha \perp, \beta)}{N(\alpha, \beta) + N(\alpha \perp, \beta \perp ) + N(\alpha, \beta \perp) + N(\alpha \perp, \beta)}
\end{align}
$$

$$
\begin{align}
S = E(a,b) - E(a,b') + E(a',b) + E(a',b')
\end{align}
$$

CHSH Bell inequality has $S \leq 2$

$$
\begin{align}
\ket{\psi_{DC} }= a \ket{H} _{s}H_{i} + be^{i\phi}\ket{V} _{s}  \ket{V } _{i}    
\end{align}
$$
---
## 7. Removing the cable phase (calibration)

  

### The correction factor

  

The directional coupler sits at the input end of the transmission line, so it compares the incident wave *entering* the line with the reflected wave *coming back out* of it. The reflected wave has crossed the line twice (down to the load, then back), so it has picked up twice the one-way phase of the line:

  

$$

\begin{align}

\Gamma_{meas}(f) = \Gamma_{L}(f)\, e^{-j2\omega T_d}

\end{align}

$$

  

So yes, the phase is doubled because the wave goes back and forth. To calibrate, multiply the exported data by the inverse:

  

$$

\begin{align}

\Gamma_{cal}(f) = \Gamma_{meas}(f)\, e^{+j2\omega T_d}, \qquad T_d = 4.1667\ \text{ns}

\end{align}

$$

  

This is the handout's $e^{+jkx}$ with $kx = \omega T_d$ for one pass, applied once for each direction. The line is lossless, so only the phase changes; $|\Gamma|$ is the same before and after.

  

The rotation $2\omega T_d$ at each design frequency:

  

| Frequency | $2\omega T_d$ | Net rotation (mod 360°) |

|---|---|---|
| 1 MHz | 3.0° | 3.0° |
| 5 MHz | 15.0° | 15.0° |
| 10 MHz | 30.0° | 30.0° |
| 100 MHz | 300.0° | 300.0° (same as −60°) |
| 1 GHz | 3000° | 120° |

  

This is why the uncalibrated angles at 10 MHz were about 30° below the hand calculations, and why the 100 MHz and 1 GHz angles looked unrelated to them.

  

### Results

  

Each simulated point is read at the sweep sample closest to the design frequency. "Analysis" is $\Gamma = (Z_L - 50)/(Z_L + 50)$ from the theory section.

  

| Load | Frequency | Uncalibrated $\Gamma$ | Calibrated $\Gamma$ | Analysis |

|---|---|---|---|---|

| 120 Ω | 1 GHz (mid-sweep) | 0.412∠−121.2° | 0.412∠−0.6° | 0.412∠0.0° |

| 120 Ω + 2 µH series | 10 MHz | 0.672∠−4.3° | 0.672∠25.7° | 0.680∠24.4° |

| 25 Ω + 2 µH series | 10 MHz | 0.866∠13.5° | 0.866∠43.5° | 0.875∠42.1° |

| 10 Ω + 1 nF series | 5 MHz | 0.753∠−128.3° | 0.753∠−113.3° | 0.753∠−113.5° |

| 2 nF | 1 MHz | 1.026∠−57.5° | 1.026∠−54.5° | 1.000∠−64.3° |

| 50 Ω ∥ 5 nH | 1 GHz | 0.615∠10.1° | 0.615∠128.6° | 0.623∠128.5° |

| 300 Ω ∥ 10 pF | 1 GHz | 0.966∠97.0° | 0.966∠−144.5° | 0.970∠−144.8° |

| (30 Ω ∥ 50 nH) + 20 pF | 100 MHz | 0.785∠−13.4° | 0.785∠−73.4° | 0.794∠−73.5° |

  

After calibration, seven of the eight loads agree with analysis to within about 0.01 in magnitude and 1.5° in phase. The 2 nF capacitor at 1 MHz does not: it is off by about 10° and reports $|\Gamma| > 1$, which a passive load cannot have.

  

### Why the low-frequency points are worse

  

The remaining error is the directional coupler, not the cable. The coupler is built from 1 µH and 100 µH coupled inductors, and it only behaves ideally when the 100 µH shunt winding is a much larger impedance than 50 Ω:

  

| Frequency | $\omega \cdot 100\ \mu\text{H}$ | Residual error after calibration |

|---|---|---|

| 1 MHz | 628 Ω | ~10° and $|\Gamma| = 1.026$ |

| 5–10 MHz | 3.1–6.3 kΩ | ~0.01 and ~1.3° |

| 100 MHz – 1 GHz | 63–628 kΩ | under 0.01 and under 0.6° |

  

At 1 MHz the shunt winding is only about 12× the line impedance, so it loads the line and the coupler no longer cleanly separates forward and reverse waves. A phase-only cable correction cannot remove that. Scaling the coupler inductors up (for example 100 µH and 10 mH, keeping the 1:10 turns ratio) would fix it in simulation; a real VNA calibration with short/open/load standards removes this kind of error as well as the cable phase.

  

### Notes on the earlier comparisons

  

- **120 Ω + 2 µH and 25 Ω + 2 µH at 10 MHz.** The earlier estimate used the one-way shift $\omega T_d = 15°$, which left the angles about 15° apart. With the round-trip 30° they agree: 25.7° vs 24.4°, and 43.5° vs 42.1°.

- **(30 Ω ∥ 50 nH) + 20 pF.** The simulation section compares this load against 0.96∠−144°, which is the 300 Ω ∥ 10 pF answer. The value calculated for this load in the theory section is 0.79∠−73.45°, and the calibrated simulation gives 0.785∠−73.4°.

- **300 Ω ∥ 10 pF.** The final answer 0.96∠−144° is right, but the intermediate impedance line is not. At 1 GHz, $Y = 1/300 + j0.0628$ S, so $Z = 0.84 - j15.9\ \Omega$.

- **120 Ω.** Before calibration this was a full circle of radius 0.41 traced about 3.3 times across 0.8–1.2 GHz. After calibration it collapses to a point at $z = 2.4$ on the real axis, as analysis predicts.

  

### Plots

  

In each figure: grey dashed is the uncalibrated export, blue is calibrated, black dotted is analysis across the sweep. The red dot is the calibrated value at the design frequency and the black × is the analytic point.

  

#### 120 Ω

![[120gamma_cal.png]]

  

#### 120 Ω in series with 2 µH, 10 MHz

![[120r2mul_cal.png]]

  

#### 25 Ω in series with 2 µH, 10 MHz

![[25r2mul_cal.png]]

  

#### 10 Ω in series with 1 nF, 5 MHz

![[10r1nc_cal.png]]

  

#### 2 nF, 1 MHz

![[2n_cal.png]]

  

#### 50 Ω in parallel with 5 nH, 1 GHz

![[50r5nl_cal.png]]

  

#### 300 Ω in parallel with 10 pF, 1 GHz

![[300r10pc_cal.png]]

  

#### (30 Ω ∥ 50 nH) in series with 20 pF, 100 MHz

![[crazy_cal.png]]

  

### Code

  

The plots and table come from `calibrate.py` in this folder. The calibration itself is one line:

  

```python

g_cal = g_raw * np.exp(2j * 2*np.pi * f * 4.1667e-9)

```