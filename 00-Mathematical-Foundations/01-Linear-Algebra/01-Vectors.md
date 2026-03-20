# **Vectors**

## 1. Definition: 

A vector is an element of a vector space that transforms according to specific rules under a change of coordinates.
In Euclidean space, vectors are often visualized as quantities with magnitude and direction.
 
##  2. Physical significance :

Vectors represent physical quantities in a way that is independent of the observer’s coordinate system.
They provide a unified framework to describe multidimensional physical quantities using components relative to a chosen basis.
Examples :
- Position and Displacemnt
- Velocity and Acceleration
- Force and Momentum
- Electric and Magnetic Fields etc.
               
## 3. Insights:

Coordinate Invariance:
Under a change of coordinates, the components of a vector change, but the vector itself remains invariant.
For rotations (orthogonal transformations), the magnitude of the vector is preserved.

Zero vector:
The unique vector with zero magnitude. It acts as the additive identity in a vector space.

## 4. Mathematical Structure:

A vector is an element of a vector space defined over a field (typically ℝ or ℂ), equipped with vector addition and scalar multiplication.

A vector space satisfies:
- Closure under addition and scalar multiplication
- Associativity and commutativity of addition
- Existence of a zero vector (additive identity)
- Existence of additive inverses
- Distributive properties

## 5. Geometric Interpretation:

Although vectors are often represented as arrows, they are fundamentally abstract objects independent of visualization.

Geometrically, vectors can represent:
- Displacement
- Directional flow
- Orientation in space

## 6. Coordinate Representation

In a chosen basis {e₁, e₂, e₃}, a vector can be written as:

v = v₁ e₁ + v₂ e₂ + v₃ e₃

The components depends on the chose of basis, but geometric vector does not.
   
## 7. Transformation 

Under a change of basis represented by a transformation matrix R, the components of a vector transform as:

$$    
\vec{v'}= R\vec{v}
$$

where R is the transformation matrix relating the old basis to the new basis.
The components change, but the underlying vector remains invariant.
This property ensures that physical laws under vectors are independent of coordinate systems.

## Computational Perspective

Vectors are represented as arrays of numbers in numerical computations.

Many physical problems reduce to vector operations such as:
- Matrix-vector multiplication
- Eigenvalue problems
- Solving systems of linear equations

These form the basis of numerical simulations in physics.
    
### Vectors provide a coordinate-independent way to represent physical quantities, ensuring that physical laws remain invariant under transformations.
