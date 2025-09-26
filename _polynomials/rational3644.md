---
layout: polypage
title: Exact polynomial sum of squares decompositions
author: S. Laplagne
name: laplagne2023
tags: [nonnegative, sos-decomposition, rational]
---

In the paper Exact polynomial sum of squares decompositions, by J. Capco, S. Laplagne and C. Scheiderer (unpublished) we give two examples of polynomials over Q that are
sums of squares over R but not over Q. The coefficientes of the summands are in an algebraic extension of Q of odd degree 3.

The examples are simpler than the original example in the paper Facial Reduction for Exact Polynomial Sum of Squares Decompositions, by S. Laplagne.
We provide one example with $(n,2d) = (3,6)$ and another example with $(n,2d) = (4,4)$. In both cases the polynomials are sums of 3 squares.

## Maple code for the example $(n,2d) = (3,6)$

´´´
# Define t as the real root of X^3 - 2
t := RootOf(X^3-2, index=1):

# The original polynomials p1, p2, p3
p[1] := 2*t^2*x0*x2^2-2*t^2*x1*x2^2+2*t*x0^2*x2-2*t*x0*x1*x2-x0^2*x1-2*x0^2*x2+4*x0*x1*x2+2*x0*x2^2+2*x1^3+2*x1^2*x2-x1*x2^2-6*x2^3;
p[2] := 2*t^2*x0*x2^2-2*t^2*x1*x2^2+2*t*x0*x1*x2-2*t*x1^2*x2+x0^3-2*x0*x1^2-4*x0*x1*x2-3*x0*x2^2+2*x1*x2^2+6*x2^3;
p[3] := (2*(t^2*x0+t*x1+t*x2-x0+x2))*x2*(x0-x1);

# f is the sum of squares
f := simplify(add(p[i]^2, i = 1 .. 3));
f := x0^6-3*x0^4*x1^2-4*x0^4*x1*x2+2*x0^4*x2^2-8*x0^3*x1^2*x2-8*x0^3*x1*x2^2+28*x0^3*x2^3+4*x0^2*x1^3*x2+10*x0^2*x1^2*x2^2+24*x0^2*x1*x2^3+41*x0^2*x2^4+16*x0*x1^4*x2+32*x0*x1^3*x2^2-48*x0*x1^2*x2^3-120*x0*x1*x2^4-60*x0*x2^5+4*x1^6+8*x1^5*x2-12*x1^3*x2^3-15*x1^2*x2^4+36*x1*x2^5+72*x2^6;
´´´

## Maple code for the example $(n,2d) = (4,4)$

´´´
# Define t as the real root of X^3 - 2
t := RootOf(X^3-2, index=1):

# The original polynomials p1, p2, p3
p[1] := -4*t^2*x^2+4*t*x^2-2*w^2+2*w*z-2*x^2+y^2-2*y*z;
p[2] := -4*t^2*x^2-4*t*x^2+2*w^2+2*w*z+6*x^2+y^2+2*y*z;
p[3] := (4*(t^2*w+t*y+z))*x;

# f is the sum of squares
f := simplify(add(p[i]^2, i = 1 .. 3));
f := 8*w^4+32*w^2*x^2+16*w^2*y*z+8*w^2*z^2+64*w*x^2*y+16*w*x^2*z+8*w*y^2*z+40*x^4+8*x^2*y^2+32*x^2*y*z+16*x^2*z^2+2*y^4+8*y^2*z^2;
´´´

