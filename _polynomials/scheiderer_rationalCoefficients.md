---
layout: polypage
title: Sums of Squares of Polynomials with Rational Coefficients
author: C. Scheiderer
name: scheiderer2013
tags: [nonnegative, sos-decomposition, rational]
year: 2013
---

In the paper Sums of Squares of Polynomials with Rational Coefficients, C. Scheiderer gives the first examples of a sum of squares of polynomials over $Q$ that are sums of squares of polynomials over $R$, but not over $Q$.
This answers an open question by B. Sturmfels.

He gives a general construction that can be used to produce many examples. The following explicit example is given in the paper:
$$
f = x_0^4 + x_0 x_1^3 + x_1^4 - 3x_0^2 x_1 x_2 - 4x_0 x_1^2 x_2 + 2x_0^2 x_2^2 + x_0 x_2^3 + x_1 x_2^3 + x_2^4
$$

### Maple code for the example
```ruby
# Sum of squares of two polynomials
f := x[0]^4 + x[0]*x[1]^3 + x[1]^4 - 3*x[0]^2*x[1]*x[2] - 4*x[0]*x[1]^2*x[2] + 2*x[0]^2*x[2]^2 + x[0]*x[2]^3 + x[1]*x[2]^3 + x[2]^4;
```

