---
layout: polypage
title: Nonnegative polynomials and sums of squares
author: G. Blekherman
name: blekherman2012
tags: [nonnegative, sos-decomposition, positive-boundary]
year: 2012
---

The paper Nonnegative polynomials and sums of squares characterizes polynomials in the positive boundary of the SOS cone for the cases $(n,2d) = (3,6)$ and $(n,2d) = (4,4)$, and proposes a strategy to construct such polynomials.

We give an example for each case.

Case $n = 4$, $2d=4$. Sum of $4$ polynomials with unique SOS decomposition.

```
p[1] := x1^2- x4^2;
p[2] := x2^2- x4^2;
p[3] := x3^2- x4^2;
p[4] := -x1^2 - x1*x2 - x1*x3 + x1*x4 - x2*x3 + x2*x4 + x3*x4;

f := add(p[i]^2, i = 1..4);
f := 2*x1^4+2*x1^3*x2+2*x1^3*x3-2*x1^3*x4+x1^2*x2^2+4*x1^2*x2*x3-4*x1^2*x2*x4+x1^2*x3^2-4*x1^2*x3*x4-x1^2*x4^2+2*x1*x2^2*x3-2*x1*x2^2*x4+2*x1*x2*x3^2-6*x1*x2*x3*x4+2*x1*x2*x4^2-2*x1*x3^2*x4+2*x1*x3*x4^2+x2^4+x2^2*x3^2-2*x2^2*x3*x4-x2^2*x4^2-2*x2*x3^2*x4+2*x2*x3*x4^2+x3^4-x3^2*x4^2+3*x4^4;
```

Case $n = 3$, $2d=6$. Sum of $3$ polynomials with unique SOS decomposition.
The following example is given in Reznick (1978) paper

```
p[1] := x * (3/2 * x^2 - (y^2+z^2));
p[2] := y * (3/2 * y^2 - (x^2+z^2));
p[3] := z * (3/2 * z^2 - (x^2+y^2));
f := add(p[i]^2, i = 1..3);
f := (9/4)*x^6-2*x^4*y^2-2*x^4*z^2-2*x^2*y^4+6*x^2*y^2*z^2-2*x^2*z^4+(9/4)*y^6-2*y^4*z^2-2*y^2*z^4+(9/4)*z^6;
```

The following code can be used to verify the examples.
When we maximize a linear functional we will get a solution in the border, with low number of polynomials in the decomposition. 
When we maximize the smallest eigenvalue, we will get a solution wil largest possible number of polynomials in the decomposition.

If we get in both cases the same decomposition, it means that the decomposition is unique.

```
# We verify uniqueness numerically
out := exactSOS(f, facial = "no", objFunction = "random"):
eig(out[3]);

out := exactSOS(f, facial = "no", objFunction = "eig"):
eig(out[3]);
```

<!-- add history, minimal number of squares, references, verification scripts, etc. -->
