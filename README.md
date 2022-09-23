# linear-congruential-generator-cracker

### This is my implementation of a program that finds the coefficients "a", "b" and "m" by four consecutive terms of a linear congruent sequence (x0, x1, x2, x3)

## How it works?

+ Three pairwise differences of neighboring elements are made from a given sequence:
  + x1 - x0 = u0
  + x2 - x1 = u1
  + x3 - x2 = u2
  + *These calculations allow you to remove the unknown variable "b" from expressions
+ There is expression: |u2\*u0 - u1\*u1| = "*u_*", which, according to number theory, gives a number that is a multiple of the number "m"  

