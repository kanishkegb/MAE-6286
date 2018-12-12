# Presentations
### MAE6286-2018-09-18
* observed order of convergence
* refinement ratio
* LTE - p.9
* GTE - p.10
* intro to PDEs - all equations summary p.15

### MAE6286-2018-10-02
* Definitions of consistency, stability, and convergence

### MAE6286-2018-10-16
* If the numerical diffusion coefficient is negative, the solution will be unstable
* FTCS is unstable for linear convection (unconditionally unstable) p.10
* von Neumann stability analysis p.11
* conservation laws p.16

### MAE6286-2018-10-16
* classification of PDEs
* upwind schemes: BS - unstable for negative waves, numerical scheme should have the same directionality p.17

### MAE6286-2018-10-30
* Lax-equivalence theorem: For a well-posed I.V.P. and a consistent discretization scheme, stability is the necessary and sufficient condition for convergence.
* **go through this again**

### MAE6286-2018-11-06
* Backward Euler method (implicit): u^(n+1) = u^n + Δt RHS^(n+1) p.12
* BCs for implicit method
* [A][x] = [b] + [BCs]: LHS set at the beginning, RHS updated every time step p.15
* stability of implicit schemes: unconditionally stable, but stability does not mean the convergence

### MAE6286-2018-11-13
* 2D stability: σx + σy ≤ 12

### MAE6286-2018-11-20
* Crank-Nicolson: semi-implicit scheme, second-order accurate in time
* CS scheme
* All-in-one explanation p.7

### MAE6286-2018-11-27
* elliptic equations: no time-dependence (steady-state solution), driven by BCs
* 2D Laplace p.6
* Jacobi method p.8
* L2-norm p.12
* second-order Neumann condition p.15

### MAE6286-2018-12-04
* summary of relaxation methods with equations p.12

# Module 1
### Lesson 1
* Phogoid mode - intro

### Lesson 2
* First-order systems
* Euler step
* L1 norm (analytical solution)

### Lesson 3
* L1 norm (no analytical solution / grid convergence)
* Order of convergence

### Lesson 4
* Second-order methods: explicit midpoint method / modified Euler method / RK2 method
* Multi-step methods: 


# Module 2
### Lesson 1
* 1D linear convection
* Spatial discretizing: forward, backward, central
* Spatial truncation error

### Lesson 2
* CFL condition

### Lesson 3
* 1D diffusion
* Discretizing 2nd order derivatives
* Stability of diffusion equation

### Lesson 4
* Burgers' equation
* SymPy: diff, lambdify
* Animations: update

# Module 3
### Lesson 1
* Conservation laws
* Traffic flow model
* FTBS

### Lesson 2
* Lax-Friedrichs: convection > FTCS is unstable; this stabilizes FTCS by replacing rho_i^n by its average; but introduces 1st order error
* Lax-Wendroff: first scheme ever to achieve 2nd-order accuracy in both space and time; captures the sharpness of the shock; makes an overshoot; needs to calculate expensive Jacobian every time step
* MacCormack: two steps; predictor and corrector; 
* Odd-even coupling: staircase behavior on the leading edge of the wave
* Taylor series expansion

### Lesson 3
* Better flux model
* SymPy: equation solving

### Lesson 4
* Finite volume method
* 

# Module 4
### Lesson 1
* Parabolic PDEs
* Diffusion: eg. heat conduction
* FTCS
* Dirichlet BC
* Neumann BC
* Explicit schemes: need small step sizes, BC changes affect the next time step

### Lesson 2
* Implicit method - 1D

### Lesson 3
* 2D - heat conduction
* 2D stability
* pyplot.contourf

### Lesson 4

### Lessson 5
* Crank-Nicolson scheme: second-order method in both time and space (all others first-order in time and second-order in space)
* 

# Module 5
### Lesson 1
* Elliptic PDEs
* Possion's equation: `u` is unknown, `f` a function of space, need all BCs
* Laplce's equation: `f=0` (homogeneous case)
* Studey of solutions to Laplace's eqn = potential theory; solutions = potential fields
* Jacobi method: simplest relaxation scheme, worst iterative solver
* 3D surface plots + colormaps
* normalized L2 norm
* Dirichlet conditions are order-agnostic

### Lesson 2
* Possion equation: source term = RHS
* Algebraic convergence
* Spatial convergence: Dirichlet boundaries are "exact" and will never impact spatial convergence

### Lesson 3
* %%timeit
* Gauss-Seidal: 2x faster than Jacobi method
* Numba - JIT with nopython: `@jit(nopython=True)`
* SOR (Successive over-relaxation): improve on the Gauss-Seidel method by using in the update a linear combination of the previous and the current solution
* SOR stable only for `0<ω<2`: `ω = 1` = Gauss-Seidal, `ω < 1` = under relaxation, `ω > 1` = over relaxation (must converge fater than GS)
* Tuned SOR: over-relax the solution as much as possible without introducing instability
* Decay of the difference between iterates

### Lesson 4
* Steepest descent:  two successive jumps are orthogonal, not too good when used with large systems or more complicated right-hand sides in the Poisson equation
* Conjugate gradient (CG): residual
