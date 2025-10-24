# Data Driven Modeling of Complex Aerospace Systems and Fluid Flows (AS5401)
## Aim
To linearize the Unipolar/ Bipolar EHD (coupled non-linear PDE's- without Navier Stokes) through single and multiparameter DMD and further apply SINDy to get the governing equations from the data.
## Description
From OpenFOAM solver (\vec{u} = 0), the bipolar species equations shall be solved in one-dimensional system (two-dimensional geometry) to acquire the species variations for various M, Co etc., and considering the Onsager function to be neglected.
## TODO
- [x] Decide the governing equations and variables
    - [x] Refer Vazquez2019, a1R9, ehdFoam_b1R8. (Equ. 41-44 **NOT WORKING**- due to negative species in the domain- **Suspect on Numerical instability**).
    - [ ] Refer Vazquez2013, a0R5, ehdFoam_b0R8. (Equ 2-6, 18, 19)
        - Variables: T, C, M
        - $T = \dfrac{\epsilon \phi_0}{\rho\nu K}, \quad C = \dfrac{q_0 d^2}{\epsilon \phi_0}, \quad M = \dfrac{1}{K}\sqrt{\dfrac{\epsilon}{\rho}}$.
        - Variable: $q_0, K, \phi_0$ and constants: $\epsilon, \rho, \nu, d$ for this case
- [x] Decide the governing equations and variables (Unipolar Injection)
- [x] Acquire the suitable solver/ case (a0R5, ehdFoam_b0R8)
- [x] Verify the solver, geometry, parameters, schemes, solution controls (Refer a0R5)
- [ ] Pre trail runs
    - [ ] Generate a small snapshot matrix for single parameter
        - Co = 0.1, 0.2, till 1.0
        - Data along X axis (1D)- Np, Nn, potentialDifference
    - [ ] Run the DMD and see if it can reproduce your data
    - [ ] See if DMD can predict the unseen data (not so important)
    - [ ] Prepare the SINDy code (dNp/dt = dNn/dt = 0)- set the RHS of SINDy equation to zero for discovery
    - [ ] Verify the equation
    - [ ] Multi parameter DMD and SINDy stratergy
    - [ ] TRY TO ADD MORE ON THIS PART
- [ ] Write the Proposal on this upto decided
- [ ] Plan the main trial runs (based on difficulties in pre-trail runs)

## References
[Vazquez2019]- 10.1063/1.5121164