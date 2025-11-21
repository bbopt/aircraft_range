# Aircraft range: A supersonic business jet MDO problem

C++ implementation of the multidisciplinary design optimization (MDO) problem described in:

Sobieszczanski-Sobieski, Agte and Sandusky, *Bi-Level Integrated System Synthesis (BLISS)*. NASA/TM-1998-208715, 1998.

The blackbox executable performs a multidisciplinary design analysis (MDA) of a coupled system of disciplines: structures, aerodynamics and propulsion. The objective is maximize the aircraft range computed using the Breguet range equation. The discipline computation relies on analytical expressions typical for an early conceptual design stage.

Two variants of the blackbox are available, depending on how the MDA is managed for solving the disciplines coupling: (I) The coupling can be solved internally within the blackbox source code using a *fixed-point iterative method*. (II) Alternatively, the backward discipline coupling can be broken by introducing additional variables and *consistency equality constraints*. Note that the second variant necessitates an optimization algorithm capable of handling equality constraints effectively.

## Problem specifications

For fixed point iterative variant (I)
- Input dimension: **10**
- Number of inequality constraints: **10**
- Inequality constraints must satisfy the form: **gᵢ(x) ≤ 0**

For the consistency constraints variant (II) three additional variables and equality constraints are added 
- Input dimension: **13**
- Number of inequality constraints: **10**
- Number of equality constraints: **3**
- Consistency equality constraints (II) must satisfy the form: **hᵢ(x) = 0**. 


### Initial points
Ten different initial points are provided.

### Variable bounds
All variables are scaled and bounded between 0 and 100. 


