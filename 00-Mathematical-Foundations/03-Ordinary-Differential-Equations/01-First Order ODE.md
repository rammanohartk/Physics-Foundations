# First-Order Ordinary Differential Equations

## Mathematical Definition

A first-order ODE has the general form:

$$
\frac{dy}{dt} = f(t,y)
$$

The highest derivative present is the first derivative.

### Special important case (linear first-order):

$$
\frac{dy}{dt} + p(t) y = g(t)
$$

If g(t)=0, the equation is homogeneous.

## Geometric Interpretation

A first-order ODE defines a slope field.

At each point (t, y), the equation assigns a slope dy/dt.

The solution is a curve whose tangent matches this slope at every point.

For non-autonomous systems:
- The system evolves in (t, y) space

For autonomous systems (dy/dt = f(y)):
- The system can be visualized on a one-dimensional phase line

So geometrically:
- The system moves along a one-dimensional trajectory.
- Phase space is one-dimensional (just y).
- There is no independent velocity variable.
- This is the simplest type of dynamical flow.

## Physical Meaning

A first-order ODE describes systems where the rate of change depends only on the current state and time:

dy/dt = f(t, y)

Such systems do not explicitly include higher-order effects like acceleration.

They often model relaxation, growth, or decay processes.

The absence of higher derivatives means that the system does not explicitly model inertia or momentum effects.

### Physical Examples

#### Radioactive Decay
dN/dt = −λN
Decay rate depends only on current amount.
---

#### RC Circuit (Discharge)
dQ/dt = −(1/RC) Q
Charge decreases exponentially.
---

#### Newton’s Law of Cooling
dT/dt = −k (T − T_env)
Temperature approaches equilibrium exponentially.

### Physical Properties

For simple first-order systems:

- Typically approach equilibrium monotonically
- Do not exhibit oscillations on their own

Oscillatory behavior generally requires at least second-order dynamics or coupling between variables.
(Why? - Because there is no second derivative (no inertia). They lack stored kinetic energy.)

## Solution Methods

### 1.Separation of Variables

If:

dy/dt = g(t) h(y)

Then:

dy/h(y) = g(t) dt

Integrating both sides yields the solution.

This process can be interpreted as :
- This method separates dependence on variables and accumulates their effects through integration.

### 2.Integrating Factor (Linear Case)

For:

dy/dt + p(t) y = g(t)

Multiply by integrating factor:

μ(t) = e^{∫ p(t) dt}

This gives:

d/dt (μy) = μ g(t)

which can be integrated directly.

This process can be interpreted as:
- The integrating factor compensates for the varying coefficient, transforming the equation into an exact derivative.

## Computational Perspective

First-order ODEs are straightforward to simulate numerically.

Common methods:
- Euler method
- Runge–Kutta methods
- Adaptive solvers

Only one initial condition is required:

y(t₀) = y₀

So computationally,
- Their simplicity often leads to stable numerical behavior, though nonlinear systems may still present challenges.

## My thoughts

The first order ODEs are the systems that fade, grow or relax. The processes are irreversible(decay,dissioation). If any system oscillates it cannot be purely first order as there is no inertia in first order ODEs.    