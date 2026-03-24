# modelling_mental_synthesis_2
A Study of the Plastic Kuramoto Model and its Capacity to Model Mental Synthesis
This repository explores the computational dynamics of Mental Synthesis—the cognitive ability to combine independent mental images into novel mental images through oscillator physics.
The project evolves from simulating the standard Kuramto model to novel two-population models with Spike-Timing-Dependent Plasticity (STDP).

Post-MSc Evolution: Performance Optimization
Initially developed during my MSc using standard Python loops and built-in SciPy solvers, this codebase has been refactored to meet industry standards for high-performance computing:
Vectorisation: Replaced iterative loops with NumPy broadcasting to handle large-scale oscillator matrices.
Numba Integration: Utilised @njit (Just-In-Time compilation) to bring Python execution speeds close to C++.
Custom Solvers: Implemented a manual Runge-Kutta (RK4) solver to bypass the overhead of generic library solvers, allowing for massive parallelisation of the Kuramoto-Sakaguchi equations.

Study Roadmap
The project is structured into six progressive stages:
Fundamental Kuramoto Model: Basic phase synchronization and the introduction of Numba acceleration.
Kuramoto-Sakaguchi Model: Confirming the theoretical onset of synchrony with phase-lag parameters.
STDP Implementation: Reproducing the plastic coupling results of Maistrenko et al.
Cyclic Coupling: Validating the findings of Ansarira et al. and Botha et al. on the emergence of chimera states and hysterisis due to the presence of a phase lag.
Random Coupling with STDP (Novel): Exploring the effect of random connections on the emergent properties of the Kuramoto-Sakaguchi model with STDP.
Two-Population Model (Novel): Investigating inter-ensemble coupling and its implications for the "Mental Synthesis" hypothesis.

Key Results & Visualisations
(Note: Since this is a simulation-only project, all data is generated in-silico.)
1. Reproducing the thermodynamic onset of synchrony for the classical Kuramoto and Kuramoto-Sakaguchi models
2. Realising a speed up factor of ~134x with the use of Numba
3. Reproduced the hysterisis loop observed for the Kuramoto model under asymmetric STDP
4. Reproduced the hystersis loop and chimera states observed by Ansariara et al. and Botha et al. for the Kuramoto-Sakaguchi model with STDP
5. Showed that the Kuramoto-Sakaguchi model with STDP under random coupling extended the phase lag range within which non-trivial memories can be represented
6. Demonstrated that the Kuramoto-Sakaguchi model with STDP for two populations connected via random coupling produces representations that allow ensemble synchronisation while retaining elements of the memories represented, representing the first mathematical model of mental synthesis 
7. Vectorised scripts and used custom solvers to bypass built in solver overhead
