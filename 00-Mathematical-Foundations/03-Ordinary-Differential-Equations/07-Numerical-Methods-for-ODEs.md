# Numerical-Methods-for-ODEs

## Mathematical Definition

An ordinary differential equation (ODE) defines time evolution:

dy/dt = f(t, y),   y(t₀) = y₀

The exact solution can be written as:

$$
y(t_{n+1}) = y(t_n) + ∫_{t_n}^{t_{n+1}} f(t, y) dt
$$

However, this integral cannot usually be evaluated exactly.

We discretize time:

$$
t_n = t₀ + nΔt
$$

and approximate:

$$
y_{n+1} ≈ y(t_{n+1})
$$

## Geometric Interpretation

An ODE defines a vector field of slopes in (t, y) space.

- True solution → smooth curve following the field  
- Numerical solution → sequence of discrete steps  

Each method approximates the area under the slope curve differently:

- Euler → straight-line approximation  
- Runge–Kutta → averaged slopes  
- Implicit methods → stability-corrected steps  

## Physical Meaning

(Why Numerical Methods Exist)
Most real physical systems are:

- Nonlinear  
- Coupled  
- Without closed-form solutions  

Analytical methods often fail.

Numerical methods approximate continuous evolution using discrete steps.

### Discrete Simulation of Continuous Physics

Nature evolves continuously, but computers simulate it step-by-step.

At each timestep:
1. Evaluate slope  
2. Estimate change over Δt  
3. Update state  

This transforms physics into a computable process.

## Core Idea

All numerical methods approximate:

$$
∫_{t_n}^{t_{n+1}} f(t, y) dt
$$

Different methods differ in how accurately they approximate this integral.

##### A simulation is a controlled approximation of continuous physics.
This shift — from exact formulas to stepwise evolution — is where computational physics begins.

## 1. Euler Method (First Order)

$$
y_{n+1} = y_n + Δt f(t_n, y_n)
$$

Idea:
- Uses slope at the beginning of the interval  
- Assumes it remains constant  

Properties:
- Order: 1  
- Fast but inaccurate  
- Unstable for oscillatory systems  

## 2. Runge–Kutta Method (RK4)

$$
y_{n+1} = y_n + (Δt/6)(k₁ + 2k₂ + 2k₃ + k₄)
$$

Idea:
- Samples slope at multiple points  
- Averages them for higher accuracy  

Properties:
- Order: 4  
- High accuracy  
- Widely used in physics simulations  

## 3. Backward (Implicit) Euler

$$
y_{n+1} = y_n + Δt f(t_{n+1}, y_{n+1})
$$

Idea:
- Uses slope at the future point  
- Requires solving an equation at each step  

Properties:
- Stable for stiff systems  
- Used in industrial solvers  

## Stability

If Δt is too large:

- Numerical energy may grow artificially  
- Solutions diverge  
- Simulation becomes unphysical  

Stability depends on:
- Method  
- Timestep (Δt)  

and not just accuracy.

## Stiffness

A system is stiff when fast and slow dynamics coexist.

Example:
- Electrons (fast)  
- Lattice motion (slow)  

Explicit methods require very small Δt → inefficient  
Implicit methods remain stable → preferred

## Error Analysis

- Local error → error per step  
- Global error → accumulated error  

If:

Error ∼ (Δt)^p

Then p is the order of the method:

- Euler → p = 1  
- RK4 → p = 4  

## My thoughts

Most of the real ODEs cannot be solved analytically. I think understanding the stability,stiffness and choice of method are the most important part than memorization of formulas. This will be a starting point where physics becomes a computable reality and I think analytical methods gives us a structure and numerical method helps us simulate the universe(transforms physical laws). Also analytical methods provide structure, while numerical methods make physics computable.


