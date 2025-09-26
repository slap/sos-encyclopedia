---
layout: polypage
title: Random polynomials of fixed degree and number of variables
name: randomPolynomials
author: S. Laplagne 
tags: [nonnegative, sos-decomposition, random]
year: 2025
---

The following code generates random polynomials with integer coefficients in a given range. 

It can be used to find typical lengths of sums of squares

#### Maple code

```ruby
nPolys := 13;
d := 2; # Degree
n := 6; # Number of variables

# Variables
polVars := [seq(x[i], i = 1..n)]; 

# Monomials
varSum := add(polVars[i], i = 1 .. nops(polVars)); 
md := expand(varSum^d); 
cfs := coeffs(md, polVars, 'ctd'); 
m2d := expand(varSum^(2*d)); 
cfs := coeffs(m2d, polVars, 'ct2d'); 
monoms := [ctd];
nMonoms := nops(monoms);

# Dice
roll := rand(-6 .. 6); 

# Random polynomials
p := [seq(add(roll()*monoms[i], i = 1 .. nMonoms), j = 1..nPolys)];

f := add(p[j], j=1..nPolys);

# We can find the length by minimizing random linear functionals 
out := exactSOS(f, facial = "no", objFunction = "random"):
eig(out[3]);
```

<!-- add history, minimal number of squares, references, verification scripts, etc. -->
