### Truncation Error (TE)

* Local TE (LTE): diff between the numerical solution u_{n+1} after one step size \Delta t and the exact solution u(t_{n+1})
LTE = u(t_n + \Delta t) - u_{n+1}
* Global TE (GTE): all LTE at a given time
u^{n+1} = ((u^n + \Delta t du/dt|_n)) + (((\Delta t ^2 /2 * du^2/d^2t|n + ( \Delta t^3))))
((Euler's method)) ((LTE))


### 1D Convection
Central difference is unconditionally unstable
