# Systems of ODEs

## Definition 

A system of ordinary differential equations (ODEs) is a collection of differential equations that describe the simultaneous time evolution of multiple unknown functions.

Instead of solving for a single function x(t), we solve for a vector of functions.

$$
x(t) = \begin{bmatrix}
x_1(t) \\ x_2(t) \\ . \\ . \\ x_n(t)
\end{bmatrix}
$$

A general first-order system has the form:

$$
\frac{dx}{dt} = f(t,x)
$$

where:

$$
x(t)∈R^n
$$
- x(t)is called the state vector
- f defines the evolution rule

The Systems arise whenever:
- Multiple degrees of freedom interact
- The rate of change of one variable depends on others
- Higher-order equations are rewritten as first order
- PDEs are discretized in space (Method of Lines)

A system of ODEs can be classified as:
- Linear
- Nonlinear

If the system is linear, it can further be classified as:
- Homogenous(no forcing term)
- Nonhommogenous(with forcing term}

### Examples 

The system evolves as a collective object in state space.
Examples include:
- Coupled oscillators
- Lattice vibrations
- Electrical circuits
- Predator–prey models
- Discretized wave equations

## Linear Systems of ODEs

A system is called linear if the evolution rule depends linearly on the state:

$$
\frac{dx}{dt} = Ax
$$

where:
A is a constant matrix

Linear systems are central because:
- They describe small oscillations
- They appear after linearization of nonlinear systems
- They govern quantum time evolution
- They arise after spatial discretization of linear PDEs

### Homogeneous Linear Systems

A linear system is called homogeneous if:

$$
\frac{dx}{dt} = Ax
$$

It is called homogeneous because:
- The right-hand side contains only the state vector
- If x=0, then x′=0
- There is no external input

This represents a closed system.
#### Solution 

The exact solution is:

$$
x(t) = e^{At} x_0
$$

If A is diagonalizable:

$$
A = PDP^{-1}
$$

Then:

$$
e^{At} = Pe^{Dt}P^{−1}
$$

The eigenvalues determines the  behavior:
- Re(λ) < 0 → decay
- Re(λ) > 0 → growth
- Imaginary λ → oscillation

#### Phase Space Interpretation
- The system defines a flow in R^n 
- Eigenvectors define invariant directions
- Long-time behavior is governed by dominant eigenvalues

### Nonhomogeneous Linear Systems (Driven Systems)

A linear system becomes nonhomogeneous when an additional forcing term is present:

​$$

\frac{dx}{dt} = Ax +b(t)

$$


where:
- A describes internal interactions
- b(t) is an external input

It is called nonhomogeneous because:
- Even if x = 0, the derivative may not be zero
- The system is influenced externally

We can say that a Homogeneous systems are a special case where: 

$$
$$
b (t) = 0
$$
#### Physical Meaning 
- Driven Systems

Examples:

- Forced pendulum
- Circuit with voltage source
- Mass under external force
- Particle in external electric field
- Real systems are almost always nonhomogeneous.

#### Solution

As the system is linear:

$$
x(t) = x_h(t) + x_p(t)
$$

- x_h transient (homogeneous solution)
- x_p forced response

General formula:

$$
x(t)= e^{At}x0+\int_0^t{e^{A(t−s)}b(s)ds}
$$

This tells us that 
- Internal dynamics propagate via matrix exponential
- Forcing accumulates over time
- The system has memory of past inputs

### Computational Physics Perspective

A system of ODE is mathematical model for  time evolving coupled variables.
Here we can turn physics into state vector and simulate how system evolves with time.

## My thoughts

As most of the physics variables are coupled it is necessery to understand system of ODEs as they can make simple computational works for coupled dynamics.



