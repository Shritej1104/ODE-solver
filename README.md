# ODE-solver
Interactive ODE solver using numpy and sympy+matplotlib 
# Interactive ODE Solver (SymPy + Matplotlib)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Shritej1104/ode-solver/blob/main/ODE_Solver.ipynb)

Solves and plots 1st/2nd order ODEs with a reusable function.

## Features
- Symbolic solving with SymPy
- Plotting with Matplotlib
- Reusable `solve_and_plot(ode_expr, c1_value=1, x_range=(0,5))`

## Example
```python
import sympy as sp
x = sp.Symbol('x'); y = sp.Function('y')
from ode_solver import solve_and_plot
ode = sp.Derivative(y(x), x) + y(x) - sp.exp(x)
solve_and_plot(ode, c1_value=1, x_range=(0,5))

