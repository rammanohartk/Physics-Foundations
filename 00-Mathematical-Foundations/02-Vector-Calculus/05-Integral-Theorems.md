# Integral Theorems

Vector Calculus contains three main fundemental integral theorems that connect local differential operators to global integral boundaries.

It is better to start with the three main types of integrals first.

## Line Integral

A line integral measures the circulation or work done along a path.
For a vector field $F$ along a curve $C$,

$$
\int_{C}F \cdot dr
$$

## Surface Integral

A surface integral measures total flow(flux) through a surface
For a surface $S$,

$$
\int_{S} F \cdot dA
$$

## Volume Integral 

Volume integral measures total quantity inside a volume
For a region $V$,

$$
\int_{V} fdV
$$

Now we can go to the 3 major theorems.
All three theorems are special cases of :
- Integral of a derivative over a region = Integral of the function over its boundary
- Derivative inside $\harr $ Quantity on boundary
- single geometric principle in different dimensions

The dimension progression of these are:
- Line $\rarr$ Area
- Area $\rarr$ Surface
- Volume $\rarr$ Surface

## 1. Green's Theorem (2D)

For a vector field $ F = (P,Q) $ in a plane,

$$
\oint_{C}(Pdx + Qdy) = \int_{A}(\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y})dA
$$

The circulation around boundary is total curl inside the region.(Stokes theorem in 2D)

## 2. Stoke's Theorem(3D)

The circulation along boundary curve is surface integral of curl(Curl theorem)
$$
\int_{S}(\nabla \times F) \cdot A = \oint_{\partial S} F \cdot dr
$$ 

## 3. Gauss' Divergence Theorem

The volume integral of divergence is the flux through boundary surface(divergence theorem)

$$
\int_{V}(\nabla \cdot F)dV = \oint_{\partial V}F \cdot dA
$$

## Geometric Interpretaion

The main idea is that the interior behavior is encoded in the boundary.
In Green's Theorem 
- total microscopic rotation inside are = circulation along edge
In Stoke's Theorem
- total rotation over surface = boundary circulation
In Gauss' Theorem
- total volume expansion = net outward flow

## Physical Meaning

Integral theorems explain conservation laws i.e, what leaves a region must reduce whats inside.
### Line integral $\rarr$ Work

$$
\int_{C}F \cdot dr
$$

measures work done by a force field and by Stoke's theorem 
-if curl = 0, work becomes path independent

### Flux $\rarr$ Source strength

$$
\int_{S} F \cdot dA
$$

measures total flow through surface and Gauss' theorem explains why
- if divergence is positive inside, there must be outword flux

Used in:
- Gauss's law
- fluid flow conservation
- continuity equations

### Circulation $\rarr$ Rotation

Stokes theorem explains
- if curl is nonzero, there mmust be ciculation along boundary.

Used in:
- Maxwell's equations
- electromagnetic induction

## Computational Uses

Integral theorems are the bcakbone of numerical physics and some examples are 
- finite volume methods
- fnite element methods
- ensure conservation laws

## My thoughts

Integral theorems can be considered as a geometry based physics as it talks about how local physics creates global physical effects like divergence creates flux and curl creates ciculation.
