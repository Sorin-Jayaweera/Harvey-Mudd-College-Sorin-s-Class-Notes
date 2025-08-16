Typically people use a linear polarized drive term (co rotating and counter rotating terms). They swith to a counter rotating frame and make approximations. But this is only valid if Drive strength << drive frequency. 

Where this isn't valid, i.e. capacitor and inductor and (box with a cross) are shunted to ground in parallel.

Challenging to analytically compute the time evolution, and evolution depends on absolute time. 

The rotating wave approximation has a cosine and sign wave with the same frequency and some offset, which we multiply by real and imaginary terms that correspond to a number $\epsilon$ that has a an imaginary correction term and a real drive term (neat way of encoding coefficients!).

Anharmonic? Very large, in the GHz range. Strong coupling to the cubit levels. 

Focus on charge driving so that all the coupling is given by the drive charge ......

- [ ] Drive strength
- [ ] $\lambda$ proportionality constant
- [ ] tuning


How do we calibrate and do in experiment?

Try using computing with no error correction, orbit that minimizes error, and deterministic that has RWA errors and computational levels.
![[20250317_114832 1.jpg]]


They found best results by using orbit correction for small time step, then using deterministic error correction for coherent errors. They numerically find estimates from the coherent error and compare with deterministic and orbit.

What is leakage rate?
![[20250317_114832.jpg]]

