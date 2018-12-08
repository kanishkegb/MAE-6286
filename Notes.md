### Truncation Error (TE)

* Local TE (LTE): diff between the numerical solution u_{n+1} after one step size \Delta t and the exact solution u(t_{n+1})
LTE = u(t_n + \Delta t) - u_{n+1}
* Global TE (GTE): all LTE at a given time
u^{n+1} = ((u^n + \Delta t du/dt|_n)) + (((\Delta t ^2 /2 * du^2/d^2t|n + ( \Delta t^3))))
((Euler's method)) ((LTE))


### 1D Convection
Central difference is unconditionally unstable

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
* Lax-Friedrichs: convection > FTCS is unstable; this stabilizes FTCS; but introduces 1st order error
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
* Diffusion
### Lesson 2
### Lesson 3
### Lesson 4

# Module 5
### Lesson 1
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
* Spatial convergence

### Lesson 3
### Lesson 4
