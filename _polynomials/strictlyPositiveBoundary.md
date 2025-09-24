---
layout: polypage
title: Strictly positive polynomials
name: striclyPositiveBoundary
degree: 6
variables: 2
tags: [motzkin, classical, nonnegative, sos-decomposition]
---

```ruby
Maple code
w1 := 2*x0^3*x2-x0^2*x2^2-2*x0*x2^3+x2^4;
w2 := -(1/6)*x0^4+(1/6)*x0^3*x2+(1/2)*x0^2*x1^2+2*x0^2*x1*x2+(1/2)*x0^2*x2^2-(5/2)*x0*x1^2*x2-3*x0*x1*x2^2-(1/3)*x0*x2^3+(3/2)*x1^2*x2^2+x1*x2^3;
w3 := -x0^2*x1*x2+x1^3*x2;
w4 := -x0^2*x1^2+x1^4;
w5 := -x0^3*x1+x0*x1^3;
pp := (2*x0^3*x2-x0^2*x2^2-2*x0*x2^3+x2^4)^2+(-(1/6)*x0^4+(1/6)*x0^3*x2+(1/2)*x0^2*x1^2+2*x0^2*x1*x2+(1/2)*x0^2*x2^2-(5/2)*x0*x1^2*x2-3*x0*x1*x2^2-(1/3)*x0*x2^3+(3/2)*x1^2*x2^2+x1*x2^3)^2+(-x0^2*x1*x2+x1^3*x2)^2+(-x0^2*x1^2+x1^4)^2+(-x0^3*x1+x0*x1^3)^2;
````

One SOS-like decomposition (identity to check) is:
$$
M(x,y) = (x^2y - 1)^2 + (xy^2 - 1)^2 + \text{(adjustment)}.
$$

<!-- add history, minimal number of squares, references, verification scripts, etc. -->
