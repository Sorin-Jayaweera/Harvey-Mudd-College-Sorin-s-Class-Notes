
Superconducting qubit control has a common approach: amplitude modulated pulses 

There are two main categories of gates: Baseband flux gate with no carrier, and microwave gate with fixed-frequency carrier.

What about frequency modulation in addition with amplitude modulation?

Use only flux frequency qubits to avoid flux excursion
more control knobs, so greater fidelity

FM - "CHIP".
Time varying frequency is typically expressed in terms of the instantaneous frequency. 

We just need a function that gives the frequency at a point in time.

## Floquet Theory
In a nutshell: 
we have an original hilbert space where a system is evolving. We want to compute the evolution in the system, but as it becomes more complicated we need a lot of computational tools.

They introduce an extended Hilbert space where the Hamiltonian is time independent. The Hilbert space comprises of periodic functions. They define a map between the origional space and the time independent one. 

They have eigenvalues for the ket operators, quasi-energies and Floquet modes.

This embeds fast periodic components into a Fourier basis. 

The extended Hilbert space shows us more interesting interactions in the Floquet modes. 

They proposed doing individually amplitude then frequency then n frequency modulation then amplitude. This allows them to traverse the Hilbert space?


Quasiadiabatic

CZ gates 
