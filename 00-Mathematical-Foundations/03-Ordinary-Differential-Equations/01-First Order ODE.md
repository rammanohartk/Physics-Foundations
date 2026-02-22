# First-Order Ordinary Differential Equations

## Mathematical Definition

A first-order ODE has the general form:

$$
\frac{dy}{dt} = f(t,y)
$$

The highest derivative present is the first derivative.

### Special important case (linear first-order):

$$
\frac{dy}{dt} + p(t)y = g(t)
$$

If g(t)=0, the equation is homogeneous.

## Geometric Interpretation

A first-order ODE defines a slope field.

At every point (t,y), the equation assigns a slope:

$$
\frac{dy}{dt}
$$

The solution is a curve whose tangent at each point matches this slope.

So geometrically:
- The system moves along a one-dimensional trajectory.
- Phase space is one-dimensional (just y).
- There is no independent velocity variable.
- This is the simplest type of dynamical flow.

## Physical Meaning

Here we can say that a first-order equation describes a memoryless system.

The rate of change at any moment depends only on:
- The current state
- The current time

There is no inertia.
So if you remove the driving force, the system does not coast, it immediately stops evolving (or strictly decays).

### Physical Examples

- Radioactive Decay

$$
\frac{dN}{dt} = - \lambda N
$$

Decay rate depends only on current amount.

- RC Circuit (Capacitor Discharge)

$$
\frac{dQ}{dt} = - \frac{1}{RC} Q
$$

Charge decreases exponentially.

- Newton’s Law of Cooling

$$
\frac{dT}{dt} = -k(T - T_env)
$$

Temperature approaches equilibrium exponentially.

### Physical Property

First-order systems:
- Cannot overshoot equilibrium.
- Cannot oscillate.
- Approach equilibrium monotonically.

(Why? - Because there is no second derivative (no inertia). They lack stored kinetic energy.)

## Solution Methods

### 1.Separation of Variables

If the equation can be written as:

$$
\frac{dy}{dt} = g(t)h(y)
$$	​

We can separate variables as

$$
\frac{1}{h(y)} dy = g(t)dt
$$	​

Then we can integrate both sides to get solution

Ths process can be interpreted as :
- We separate cause and response, then accumulate (integrate).

### 2.Integrating Factor (Linear Case)

Here for the case,

$$
\frac{dy}{dt} + p(t)y = g(t)
$$

We multiply by integrating factor:

$$
\mu(t) = e ^{\int p(t)dt} 
$$

This  will help transform the left-hand side into a total derivative:

$$
\frac{d}{dt}(\mu y) = \mu g(t)
$$

We can integrate this directly.

This process can be interpreted as:
- The integrating factor can be a tool that can  compensate for “leakage” in the system.

## Computational Perspective

First-order ODEs are straightforward to simulate numerically.

Common methods:
- Euler method
- Runge–Kutta methods
-Adaptive solvers

As there is no velocity variable involved only one initial condition is required (as order is 1)
Only one initial condition is required:

$$
y(t_0) = y_0
​$$
So computationally,
- They are stable and predictable unless nonlinearities create sharp gradients.

## My thoughts

The first order ODEs are the systems that fade, grow or relax. The processes are irreversible(decay,dissioation). If any system oscillates it cannot be purely first order as there is no inertia in first order ODEs.    