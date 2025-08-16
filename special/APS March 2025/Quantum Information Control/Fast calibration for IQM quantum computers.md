
CZ gates with tunable couples:
fast diabatic CZ gates with flux tunable transom qubits and couplers
![[20250317_130912.jpg|500]]

QPU charaterization
Collect hamiltonian model parameters as a function of flux for both qubits and coupler before calibrating CZ gates

we have frequencies for the qubits, anharmonicities, and coupler couplings.


The most naive approach:
Model based calibration. Sweep pulse parameters and look for the optimal point. This is slow.

Instead, separate the variables and convert to a 1d problem, where from an initial guess you tune and find optimal place. This is a little risky, but  

