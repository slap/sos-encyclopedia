---
layout: polypage
title: Strictly positive polynomials
name: striclyPositiveBoundary
degree: 6
variables: 2
tags: [nonnegative, sos-decomposition]
---

Strictly positive polynomials in the boundary of Sigma(n=3, 2d=8) cone. 

Maple code
```ruby
w1 := 2*x0^3*x2-x0^2*x2^2-2*x0*x2^3+x2^4;
w2 := -(1/6)*x0^4+(1/6)*x0^3*x2+(1/2)*x0^2*x1^2+2*x0^2*x1*x2+(1/2)*x0^2*x2^2-(5/2)*x0*x1^2*x2-3*x0*x1*x2^2-(1/3)*x0*x2^3+(3/2)*x1^2*x2^2+x1*x2^3;
w3 := -x0^2*x1*x2+x1^3*x2;
w4 := -x0^2*x1^2+x1^4;
w5 := -x0^3*x1+x0*x1^3;
p := w1^2 + w2^2 + w3^2 + w4^2 + w5^2;
p := (2*x0^3*x2-x0^2*x2^2-2*x0*x2^3+x2^4)^2+(-(1/6)*x0^4+(1/6)*x0^3*x2+(1/2)*x0^2*x1^2+2*x0^2*x1*x2+(1/2)*x0^2*x2^2-(5/2)*x0*x1^2*x2-3*x0*x1*x2^2-(1/3)*x0*x2^3+(3/2)*x1^2*x2^2+x1*x2^3)^2+(-x0^2*x1*x2+x1^3*x2)^2+(-x0^2*x1^2+x1^4)^2+(-x0^3*x1+x0*x1^3)^2;
````

Strictly positive polynomials in the boundary of Sigma(n=3, 2d=10) cone. 

Maple code
```ruby
w1 := -x0^2*x1*x2^2+x1^3*x2^2;
w2 := -x0^2*x1^2*x2+x1^4*x2;
w3 := -x0^4*x1+x1^5;
w4 := -x0^3*x1*x2+x0*x1^3*x2;
w5 := -x0^3*x1^2+x0*x1^4;
w6 := -x0^4*x1+x0^2*x1^3;
w7 := 4*x0^4*x2-5*x0^2*x2^3+x2^5;
w8 := (4/15)*x0^5-(4/5)*x0^3*x1^2+2*x0^3*x1*x2-x0^3*x2^2+2*x0^2*x1^2*x2-x0^2*x1*x2^2+2*x0*x1^2*x2^2-2*x0*x1*x2^3+(1/3)*x0*x2^4-2*x1^2*x2^3+x1*x2^4;
p := w1^2 + w2^2 + w3^2 + w4^2 + w5^2 + w6^2 + w7^2 + w8^2;
p := (-x0^2*x1*x2^2+x1^3*x2^2)^2+(-x0^2*x1^2*x2+x1^4*x2)^2+(-x0^4*x1+x1^5)^2+(-x0^3*x1*x2+x0*x1^3*x2)^2+(-x0^3*x1^2+x0*x1^4)^2+(-x0^4*x1+x0^2*x1^3)^2+(4*x0^4*x2-5*x0^2*x2^3+x2^5)^2+((4/15)*x0^5-(4/5)*x0^3*x1^2+2*x0^3*x1*x2-x0^3*x2^2+2*x0^2*x1^2*x2-x0^2*x1*x2^2+2*x0*x1^2*x2^2-2*x0*x1*x2^3+(1/3)*x0*x2^4-2*x1^2*x2^3+x1*x2^4)^2
````

<!-- add history, minimal number of squares, references, verification scripts, etc. -->
