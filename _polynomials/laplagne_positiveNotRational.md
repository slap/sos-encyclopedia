---
layout: polypage
title: Sum of Squares Decomposition of Positive Polynomials with Rational Coefficients
name: striclyPositiveBoundary
author: S. Laplagne
degree: 6
variables: 2
tags: [nonnegative, sos-decomposition, positive-boundary, rational]
year: 2023
---

In the paper Sum of Squares Decomposition of Positive Polynomials with Rational Coefficients, 
we construct a polynomial over $\mathbb{Q}$ that is strictly positive and it is a sum of squares over $\mathbb{Q}$ but not over $\mathbb{Q}$.
This answers an open question by C. Scheiderer.

It is defined as the sum of 3 polynomials $h = f + g + r$, with

### A polynomial $f$ that is SOS over $R$ but not over $Q$

\begin{aligned}
p_{1} &= (-4\alpha^{2} + 4\alpha - 2)x_{0}^{2} + x_{1}^{2} - 2x_{1}x_{2} + 2x_{2}x_{3} - 2x_{3}^{2}, \\
p_{2} &= (-4\alpha^{2} - 4\alpha + 6)x_{0}^{2} + x_{1}^{2} + 2x_{1}x_{2} + 2x_{2}x_{3} + 2x_{3}^{2}, \\
p_{3} &= 4\alpha x_{0}x_{1} + 4\alpha x_{0}x_{2} + 4\alpha^{2} x_{0}x_{3},
\end{aligned}
and 
\begin{aligned}
f &= p_{1}^{2} + p_{2}^{2} + p_{3}^{2} \\
  &= 40x_{0}^{4} + 8x_{0}^{2}x_{1}^{2} + 32x_{0}^{2}x_{1}x_{2} + 64x_{0}^{2}x_{1}x_{3} + 16x_{0}^{2}x_{2}^{2} + 16x_{0}^{2}x_{2}x_{3} \\
  &\quad + 32x_{0}^{2}x_{3}^{2} + 2x_{1}^{4} + 8x_{1}^{2}x_{2}^{2} + 8x_{1}^{2}x_{2}x_{3} + 16x_{1}^{2}x_{3}^{2} + 8x_{2}^{2}x_{3}^{2} + 8x_{3}^{4}.
\end{aligned}

### A strictly positive polynomial $g$ in the boundary of the SOS cone (following a construction by G. Blekherman)
\begin{aligned}
q_{1} &= y_{0}^{2} - y_{3}^{2}, \\
q_{2} &= y_{1}^{2} - y_{3}^{2}, \\
q_{3} &= y_{2}^{2} - y_{3}^{2}, \\
q_{4} &= -y_{0}^{2} - y_{0}y_{1} - y_{0}y_{2} + y_{0}y_{3} 
         - y_{1}y_{2} + y_{1}y_{3} + y_{2}y_{3},
\end{aligned}
and 
$$
g = q_{1}^{2} + q_{2}^{2} + q_{3}^{2} + q_{4}^{2}.
$$

The resulting sum is
$$
h = f + g + (x_2^2 - y_2^2)^2
$$

### Maple code
```ruby
# The polynomial f
p[1] := (-4*alpha^2 + 4*alpha - 2)*x[0]^2 + x[1]^2 - 2*x[1]*x[2] + 2*x[2]*x[3] - 2*x[3]^2;
p[2] := (-4*alpha^2 - 4*alpha + 6)*x[0]^2 + x[1]^2 + 2*x[1]*x[2] + 2*x[2]*x[3] + 2*x[3]^2;
p[3] := 4*alpha*x[0]*x[1] + 4*alpha*x[0]*x[2] + 4*alpha^2*x[0]*x[3];
f := expand(add(p[i]^2, i=1..3));

# The polynomial g
q[1] := y[0]^2 - y[3]^2;
q[2] := y[1]^2 - y[3]^2;
q[3] := y[2]^2 - y[3]^2;
q[4] := -y[0]^2 - y[0]*y[1] - y[0]*y[2] + y[0]*y[3]
        - y[1]*y[2] + y[1]*y[3] + y[2]*y[3];
g := expand(add(q[i]^2, i=1..4));

# The polyonmial r
r := (x[2]^2 - y[2]^2)^2

# The resulting polynomial h
h := f + g + r^2;

```

<!-- add history, minimal number of squares, references, verification scripts, etc. -->
