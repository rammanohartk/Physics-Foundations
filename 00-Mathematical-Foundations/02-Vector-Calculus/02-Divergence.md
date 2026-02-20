
# Divergence ($\nabla \cdot \vec{V}$)

## Mathematical Definition:

Divergence takes a vector field and produces a scalar:

$$
\nabla \cdot \vec{V}
$$

It is the dot product between the del operator and the vector field.

## Physical Interpretation:

Divergence measures the local expansion or compression of a field.

It will give answers to: 
- Is material appearing or disappearing locally?

The common interpretation can be as :
- Positive divergence → source (outflow)
- Negative divergence → sink (inflow)
- Zero divergence → no net creation or destruction

######  note: I still does not understand fully about the aspects of divergence. I am still open to understand more about this and its applications in much detail    

An example is fluid flow 
If
$$ 
\nabla \cdot \vec{V} = 0
$$

the flow is said to be incompressible i.e, whatever enters must leave and there are no hidden sources or sinks for the flow(my understanding of this, open to other reasons) 

## Common computational usage:

Used in:
- fluid simulations
- conservation laws
- continuity equations
- incompressibility constraints