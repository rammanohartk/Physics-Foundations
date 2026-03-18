# Stability and Phase Space of ODE

## Mathematical Definition

A phase space is the set of all possible states of a system.

For a first-order system:

$$
\frac{dx}{dt} = f(x)
$$
each point x represents a complete state of the system.

The function f(x) defines a vector field, which assigns a direction of motion at every point in phase space.

A fixed point is defined by:

$$
f(x)=0
$$

where the system does not evolve.

## Geometric Interpretation

Phase space is a geometric picture of dynamics.
- Each point = a state of the system
- Each arrow = direction of evolution
- A solution = a trajectory (curve)

Instead of solving for x(t), we visualize how states flow.

Key geometric ideas:
- Fixed Points: locations where motion stops
- Trajectories: paths followed over time
- Flow Field: the full collection of arrows

## Physical Meaning

Phase space represents the complete physical state of a system, like,
- Position + velocity fully describe a particle

The ODE defines how this state changes.
So instead of tracking one solution, phase space shows all possible behaviors at once.

Types of physical behavior:
- Stable (Attractor): system moves toward equilibrium
- Unstable (Repeller): system moves away from equilibrium

## Computational Perspective

Phase space is used to analyze simulations.
- Numerical solvers generate trajectories step-by-step
- Behavior of trajectories reveals:
     - Stability
     - Long-term evolution

Important properties:
- Trajectories do not cross (deterministic systems)
- Used to study:
     - Stability of solutions
     - Sensitivity to initial conditions

Nonlinear systems may show:
- Limit cycles: closed trajectories (sustained oscillations)
- Chaotic behavior: small changes → large differences

## My thoughts
I think its better to understand Phase space as it  is the space of all possible system states and an ODE defines motion as a vector field in this space.

