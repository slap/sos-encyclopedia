---
layout: polypage
title: Facial Reduction for Exact Polynomial Sum of Squares Decompositions
author: S. Laplagne
name: laplagne2018
tags: [nonnegative, sos-decomposition, rational]
year: 2018
---

In the paper Facial Reduction for Exact Polynomial Sum of Squares Decompositions, we give a sum of squares of 3 polynomials with coefficients in algebraic extension of $Q$ of odd degree 3, such that the sum of squares has integer coefficientes, but it cannot be decomposed as the sum of squares of polynomials with rational coefficients.
This answers an open question by C. Scheiderer.

### Maple code for the example

```
p[1] := x*(2*RootOf(_Z^3-2)^2*z*x-2*RootOf(_Z^3-2)^2*z^2+2*RootOf(_Z^3-2)*x^2-2*RootOf(_Z^3-2)*x*z-2*w^2+2*w*z+y^2-2*y*z-2*z^2);
p[2] := 2*RootOf(_Z^3-2)^2*x^3-2*RootOf(_Z^3-2)^2*x^2*z+2*x^3*RootOf(_Z^3-2)-2*x^2*RootOf(_Z^3-2)*z+2*w^2*z-2*w*x*z-2*x^3+2*x^2*z-x*y^2+2*y*z^2+2*z^3;
p[3] := (2*(RootOf(_Z^3-2)^2*w+RootOf(_Z^3-2)*y+z))*x*(x-z);
f := add(p[i], i = 1..3);
```

