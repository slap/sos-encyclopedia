---
layout: polypage
title: On the Pythagoras number for polynomials of degree 4 in 5 variables
name: striclyPositiveBoundary
author: S. Laplagne
degree: 4
variables: 5
tags: [nonnegative, sos-decomposition, pythagoras]
---

In the paper On the Pythagoras number for polynomials of degree 4 in 5 variables, 
we construct a polynomial of degree $4$ in $5% variables that is the sum of 8 squares and cannot be decomposed as the sum of 7 squares.
In the paper Lengths of real forms by C. Scheiderer, the lower bound $p(5,4) = 7$ is established and we improve this bound to 8.

```ruby
p[1] := x[1]^2 - x[4]^2;
p[2] := x[2]^2 - x[4]^2;
p[3] := x[3]^2 - x[4]^2;
p[4] := -x[1]^2 - x[1]*x[2] - x[1]*x[3] + x[1]*x[4] - x[2]*x[3] + x[2]*x[4] + x[3]*x[4];
p[5] := x[1]*x[5];
p[6] := x[2]*x[5];
p[7] := x[3]*x[5];
p[8] := x[4]*x[5];
f := add(p[i], i = 1..8);
f := -x[1]*x[2]-x[1]*x[3]+x[1]*x[4]+x[1]*x[5]+x[2]^2-x[2]*x[3]+x[2]*x[4]+x[2]*x[5]+x[3]^2+x[3]*x[4]+x[3]*x[5]-3*x[4]^2+x[4]*x[5];

# We verify numerically that the SOS decomposition is unique
out := exactSOS(pp, facial = "no", objFunction = "random"):
eig(out[3]);

```

<!-- add history, minimal number of squares, references, verification scripts, etc. -->
