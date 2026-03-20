# Numerical-Methods-for-ODEs

## Mathematical Definition

An ordinary differential equation (ODE) defines how a system evolves:

$$
\frac{dy}{dt} = f(t,y), y(t_0) = y_0​
$$

Analytically, the solution is:

$$
y(t_{n+1}) = y(t_n) + \int_{t_n}^{t_{n+1}}f(t,y)dt
$$

But a computer cannot evaluate this continuous integral exactly.

So we discretize time:

$$
t_n = t_0 + nΔt
$$

and aim to compute:

$$
y_{n+1} ≈ y(t_{n+1})
$$

## Geometric Interpretation

The ODE defines a vector field of slopes in (t,y) space.
- The true solution is a smooth curve following this field
- Numerical methods approximate this curve as a sequence of small steps

Different methods correspond to different ways of approximating the area under the slope curve:
- Euler → straight-line step
- RK4 → curved, averaged step
- Implicit → stability-focused correction

## Physical Meaning

(Why Numerical Methods Exist)

Some ODEs can be solved exactly:
- Exponential growth
- Harmonic oscillator
- Simple linear systems

But most real physical systems are:
- Nonlinear
- Coupled
- Without closed-form solutions

So exact analytical solutions fail.

### The “Stop-Motion Universe”

Nature evolves continuously.
Computers simulate it in discrete frames.

At each timestep:
- Measure slope: 
- Estimate evolution over Δt
- Update state
- Repeat

##### A simulation is a controlled approximation of continuous physics.
This shift — from exact formulas to stepwise evolution — is where computational physics begins.

## Computational Perspective
Core Idea

All numerical methods approximate:

$$
\int_{t_n}^{t_{n+1}}f(t,y)dt
$$

The difference between methods is how intelligently they approximate this integral.

## 1.Euler Method (1st Order)

$$
y_{n+1} = y_n + Δt f(t_n,y_n)
$$

Idea:
- Uses slope at the start
- Assumes it stays constant

Properties:

- Order: 1
- Fast but inaccurate
- Unstable for oscillatory systems

## 2.Runge–Kutta 4 (RK4)

$$
y_{n+1} = y_n + \frac{Δt}{6}(k_1 + 2k_2 + 2k_3 + k_4)
$$

where slopes are sampled at multiple points.

Idea:
- Samples slope at start, midpoints, and end
- Averages them

Properties:
- Order: 4
- High accuracy
- Standard method in physics simulations

## 3.Backward (Implicit) Euler

$$
y_{n+1} = y_n + Δtf(t_{n+1},y_{n+1})
$$

Idea:
- Uses future slope
- Requires solving an equation at each step

Properties:
- Stable for stiff systems
- Used in industrial solvers

## Stability 

If timestep Δt is too large:
- Energy may grow artificially
- Solutions diverge
- Simulation becomes unphysical

Stability depends on method + timestep and not just accuracy

## Stiffness (Real-World Systems)

A system is stiff when:
- Fast and slow dynamics coexist

Example:
- Electrons (fast) + lattice (slow)

So and explicit methods fail unless Δt is extremely small.
Implicit methods remain stable.

## Error Concepts
- Local error → per step
- Global error → accumulated

If:

$$
Error ∼ (Δt)^p
$$

Then method is order p and
- Euler → p=1
- RK4 → p=4


## My thoughts
Most of the real ODEs cannot be solved analytically. I think understanding the stability and stiffness are the most important part than memorization of formulas.
This will be a starting point where physics becomes a computable reality and I think analytical methods gives us a structure and numerical nethod helps us simulate the universe. Also understanding how time is discretized and how stability breaks physics and the choice of method for stiffness can help in building these solvers.


