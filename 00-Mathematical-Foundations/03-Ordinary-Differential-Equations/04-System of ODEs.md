# Systems of Ordinary Differential Equations

A system of ordinary differential equations (ODEs) is a collection of differential equations that describes the simultaneous evolution of multiple variables.

Instead of a single function, we solve for a state vector:

x(t) = [x₁(t), x₂(t), ..., xₙ(t)]ᵀ

A general first-order system is:

dx/dt = f(t, x)

where:
- x(t) ∈ ℝⁿ is the state vector
- f defines the evolution rule

## When Do Systems Arise?

Systems of ODEs appear when:

- Multiple degrees of freedom interact
- Variables depend on each other (rate)
- Higher-order ODEs are rewritten as first-order systems
- PDEs are discretized in space (Method of Lines)

## Classification

A system of ODEs can be:

- Linear
- Nonlinear

Linear systems can further be:

- Homogeneous (no forcing term)
- Nonhomogeneous (with forcing)


### Examples 

The system evolves as a collective object in state space.
Examples include:
- Coupled oscillators  
- Lattice vibrations  
- Electrical circuits  
- Predator–prey models  
- Discretized wave equations  


## Linear Systems of ODEs

A linear system has the form:

dx/dt = A x

where A is a constant matrix.

These systems are central because:
- They describe small oscillations
- They arise from linearization of nonlinear systems
- They appear in quantum and classical dynamics
- They result from discretizing PDEs

### Homogeneous Linear Systems

A linear system is called homogeneous if:

dx/dt = A x

Properties:
- No external input
- x = 0 is an equilibrium solution
- Represents a closed system

### Solution

The exact solution is:

x(t) = e^{At} x₀

where e^{At} is the matrix exponential.

If A is diagonalizable:

A = P D P^{-1}

Then:

e^{At} = P e^{Dt} P^{-1}

### Eigenvalue Interpretation

Eigenvalues determine system behavior:

- Re(λ) < 0 → decay (stable)
- Re(λ) > 0 → growth (unstable)
- Imaginary λ → oscillation

Eigenvectors define invariant directions in state space.

#### Phase Space Interpretation

- The system defines a flow in ℝⁿ
- Trajectories evolve in state space
- Long-term behavior is governed by dominant eigenvalues

### Nonhomogeneous Linear Systems


A linear system becomes nonhomogeneous when an additional forcing term is present:
dx/dt = A x + b(t)

where:
- A → internal dynamics
- b(t) → external forcing

Properties:
- Even if x = 0, dx/dt may not be zero
- System is driven by external input


#### Solution (Driven System)

The general solution is:

x(t) = x_h(t) + x_p(t)

where:
- x_h → homogeneous (transient)
- x_p → particular (forced response)

Exact solution:

x(t) = e^{At} x₀ + ∫₀^t e^{A(t−s)} b(s) ds

This shows:

- Internal dynamics propagate via e^{At}
- External forcing accumulates over time
- The system retains memory of past inputs


## Computational Physics Perspective

Systems of ODEs provide a natural framework for simulating coupled physical systems.

Physics is converted into:
- A state vector (system variables)
- An evolution rule (dynamics)

Numerical integration then evolves the system in time.

This framework underlies:
- Molecular dynamics
- Circuit simulation
- Multiphysics models
- Discretized PDE solvers

## My thoughts

As most of the physics variables are coupled it is necessery to understand system of ODEs as they can make simple computational works for coupled dynamics.
They can  provide a bridge between mathematical theory and computational simulation, allowing complex coupled behavior to be studied systematically.


