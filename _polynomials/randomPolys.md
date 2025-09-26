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
d := 3; # Degree
n := 4; # Number of variables

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

f := expand(add(p[j]^2, j=1..nPolys));
```

The following code can be used to find numerically the length of the polynomials.
It minimizes a random linear functional over the spectrahedron, which gives a solution of low rank.

```
# Path for rationalSOS library
currentdir("C:/Users/slapl/Dropbox/repos/rationalSOS");

#######################################################################
# Load "Rational SOS" procedures
#######################################################################
read("rationalSOS.mpl"):
with(rationalSOS):
with(LinearAlgebra):

# Display tables of any size
interface(rtablesize=infinity);

# We can find the length by minimizing random linear functionals 
out := exactSOS(f, facial = "no", objFunction = "random"):
ev := eig(out[3]):
n := Dimension(ev):
M := < Vector(n, i -> n - i + 1) | ev >;
```

<!-- add history, minimal number of squares, references, verification scripts, etc. -->
