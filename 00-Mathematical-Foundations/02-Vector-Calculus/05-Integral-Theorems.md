# Integral Theorems

Vector calculus contains fundamental integral theorems that connect local differential behavior to global integral quantities over regions and their boundaries.

They express a deep principle:
Local derivatives inside a region ↔ Global behavior on the boundary


## Line Integral
A line integral measures work or circulation along a curve C:

For a vector field  $ F $  along a curve  $ C $,

$$
\int_{C}F \cdot dr
$$

## Surface Integral
A surface integral measures flux through a surface S:
For a surface $S$,

$$
\int_{S} F \cdot dA
$$

## Volume Integral 

A volume integral measures total quantity inside a region V:

For a region  $ V $,

$$
\int_{V} fdV
$$

Now we can go to the 3 major theorems.

### Unifying Principle

All integral theorems follow a common structure:
Integral of a derivative over a region = Integral of the field over the boundary
This reflects a single geometric principle across dimensions.

### Dimensional Progression

- 1D → 2D (Line → Area)  → Green’s Theorem  
- 2D → 3D (Surface → Boundary Curve) → Stokes’ Theorem  
- 3D → 2D (Volume → Surface) → Gauss’ Theorem

## 1. Green's Theorem (2D)

For a vector field  $ F = (P,Q) $  in a plane,

$$
∮_C (P dx + Q dy) = ∬_A (∂Q/∂x − ∂P/∂y) dA
$$

This relates circulation along a closed curve to the curl within the enclosed area.
The circulation around boundary is total curl inside the region.(Stokes theorem in 2D)

## 2. Stoke's Theorem(3D)

The circulation along boundary curve is surface integral of curl(Curl theorem)

$$
∬_S (∇ × F) · dA = ∮_{∂S} F · dr
$$ 

This relates the circulation along a boundary curve to the curl over the surface.

## 3. Gauss' Divergence Theorem

The volume integral of divergence is the flux through boundary surface(divergence theorem)

$$
∭_V (∇ · F) dV = ∬_{∂V} F · dA
$$

This relates the divergence within a volume to the flux through its boundary surface.


## Geometric Interpretation

These theorems show that interior behavior is encoded at the boundary:
- Green’s Theorem → total rotation inside = circulation along boundary  
- Stokes’ Theorem → surface rotation = boundary circulation  
- Gauss’ Theorem → total expansion inside = net outward flux


## Physical Meaning

Integral theorems underpin conservation laws.

They express that:

What leaves a region must be accounted for by what happens inside.

### Work (Line Integral)

$$
∫_C F · dr
$$

Measures work done by a force field.

If curl = 0 (conservative field), work is path independent.

---

### Flux (Surface Integral)

$$
∫_S F · dA
$$

Measures total flow through a surface.

Gauss’ theorem explains:
Positive divergence inside → net outward flux

---

### Circulation (Line Integral)
Stokes’ theorem shows:

Nonzero curl → circulation along boundary

Applications:
- Electromagnetism
- Fluid rotation

## Computational Usage

Integral theorems form the backbone of numerical physics:

- Finite Volume Methods (FVM)
- Finite Element Methods (FEM)
- Enforcing conservation laws

They allow local differential equations to be solved using global integral formulations, which are more stable numerically.

## My thoughts

Integral theorems can be considered as a geometry based physics as it talks about how local physics creates global physical effects like divergence creates flux and curl creates ciculation. This connection between local behavior and global outcomes is central to both theoretical understanding and computational modeling.
