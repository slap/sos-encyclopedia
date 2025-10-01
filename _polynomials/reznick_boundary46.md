---
layout: polypage
title: Extremal PSD forms with few terms
name: extremalPSDforms
author: Bruce Reznick
degree: 6
variables: 4
tags: [nonnegative, sos-decomposition, positive-boundary]
year: 1978
---

The first examples known to us of strictly positive polynomials in 
$\partial \Sigma_{4,6}$ appeared in the paper Extremal PSD forms with few terms by B. Reznick (1978). The author provided a construction 
for strictly positive polynomials of degree $6$ and any number of variables 
that are in the boundary of the corresponding SOS cone. For $4$ variables, 
one of such examples is 

$$
f = p_1^2 + p_2^2 + p_3^2 + p_4^2,
$$

with

$$
\begin{align*}
p_1 &= x\big((2-1/2)x^2 - (y^2 + z^2 + w^2)\big), \\
p_2 &= y\big((2-1/2)y^2 - (x^2 + z^2 + w^2)\big), \\
p_3 &= z\big((2-1/2)z^2 - (x^2 + y^2 + w^2)\big), \\
p_4 &= w\big((2-1/2)w^2 - (x^2 + y^2 + z^2)\big).
\end{align*}
$$

In the paper Strictly positive polynomials in the boundary of the SOS cone, by S. Laplagne and M.Valdettaro we prove that the polynomial $f$ has a unique decomposition as a sum of squares.

### Maple code

```
p[1] := x * ((2-1/2) * x^2 - (y^2 + z^2 + w^2));
p[2] := y * ((2-1/2) * y^2 - (x^2 + z^2 + w^2));
p[3] := z * ((2-1/2) * z^2 - (x^2 + y^2 + w^2));
p[4] := w * ((2-1/2) * w^2 - (x^2 + y^2 + z^2));
f := expand(add(p[i]^2, i = 1..4));
f := 6*x^2*y^2*z^2+6*y^2*w^2*z^2+6*x^2*w^2*z^2+6*x^2*w^2*y^2-2*x^4*w^2-2*x^4*y^2-2*x^4*z^2-2*x^2*y^4-2*x^2*z^4-2*y^4*w^2-2*y^4*z^2-2*y^2*w^4-2*y^2*z^4-2*z^4*w^2+(9/4)*x^6+(9/4)*y^6+(9/4)*z^6+(9/4)*w^6-2*w^4*x^2-2*w^4*z^2;

# We verify uniqueness
out := exactSOS(f, facial = "no", objFunction = "random"):
ev := eig(out[3]): n := Dimension(ev):
M := < Vector(n, i -> n - i + 1) | ev >;   # Only four non-zero eigenvalues
```


<!-- add history, minimal number of squares, references, verification scripts, etc. -->
