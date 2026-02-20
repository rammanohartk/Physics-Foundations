# Basis and Change of Basis

## Basis

A basis is a set of vectors that allows us to describe every vector in a space.
Any vector can be written as :

$$
\vec{v} = x\hat{i} + y\hat{j}
$$

In 2D, the standard basis are:
$$
\hat{i} = (1,0), \hat{j} = (0,1)
$$

A set of vectors is basis if:
- Spans the space (can build every other vectors)
- linearly independent

Same vector can have different bases, but the physical vector does not change only its description changes.

## Change of Basis

Change of basis means describing the same vector using different set of reference direction.
Mathematically,

$$
\vec{v'} = P^{-1}\vec{v}
$$

where $P$ contains new basis vectors.

### Geometric Insight:

This will not move the vector rather it is rotating or streching the coordinate axes.

### Why change basis?

Some of the basis makes physics simple.

In the wrong basis:
- equations will be coupled
- matrix will be messy

In right basis:
- matrix becomes diagonal
- physics becomes clear

### Connection with Diagonalization:

When we diagonalize a matrix we are doing change of basis to eigenvector basis ie,
- coupled old basis  to  independent modes.

### Imporatnce in Physics:

Basis choice can be considered as a simple language that can be used to understand physics better.
A good basis choice 
- reveals symmetry
- removes coupling
- simplifies equation
- improve numerics

### Computational Perspective:

In numerical work (including DFT):
- Hamiltonians are matrices in some basis
- Off-diagonal terms represent coupling
- Diagonalization = change of basis

So after transformation, the matrix becomes diagonal:

This improves:
- Numerical stability
- Interpretability
- Computational efficiency

So choosing a good basis often reduces complexity dramatically.

## My thought:

This topic was one of the big step I had to cover, as it is the basic step in almost every physical and computational problems. So progress in physics frequently means discovering the natural basis in which the system becomes simple. Now if I cannot understand a problems correctly I could just try change of basis to my needs as it is just the structure that I can make to understand everything in my way. I can also try to find efiicient ways in computational calculations by taking the most appropriate basis. 