
Advantages of erasure errors:
Suppose we have a surface code. If we don't have information we would apply the minimum weight correction (?), but that would get logical errors. Instead, we have erasure bits that we know. You can correct more erasure errors than unknown Pauli errors.

Erasure errors have a higher threshold, tolerating 50% erasure noise compared to 19% depolarizing noise.

Erasure qubit: Dominant noise source is detectable erasures.

But there is more to the story. Performing the erasure check is a physical operation that is imperfect that could get false positive or false negative.


Erasure - if information is corrupted, it is erased instead of looking like wrong information. But these qubits can still interact, so we have to find how to propagate error. dephasing, phase shift, etc. (?) 

## Decoding erasure circuits
Given erasure check detection events, there is an equivalent stabilizer circuit with independent error mechanisms

Any decoding method for stabilizer circuits can be used for erasure circuits. This mapping can be done exactly, so there is no loss in accuracy.

Where an error occurs, there will be poly error. Errors propagate down a line.


Erasure checks cause noise though, so we want to find the optimal frequency for checks. 

You can do it every (cycle ?) for free because the qubits are resting, but you can do it more often with chance of interrupting. This makes a threshold surface for the error rate, Pauli error rate, and classical bit flip rate. Being under the surface means you can suppress errors. 

Optimal frequency for checking erasures depends on the noise rate. 

Summary:
developed a framework to describe simulate and decode erasure qubits

simulateions of surface code and floquet codes to confirm the benefits of erasure qubits

framework explores optimization and different codes

erasure qubits are very worth it!

