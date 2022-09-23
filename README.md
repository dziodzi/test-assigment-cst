# linear-congruential-generator-cracker

### This is my implementation of a program that finds the coefficients "a", "b" and "m" by four consecutive terms of a linear congruent sequence (x0, x1, x2, x3)

## How it works?

+ Three pairwise differences of neighboring elements are made from a given sequence:
  + x1 - x0 = t0;
  + x2 - x1 = t1;
  + x3 - x2 = t2;
  + *These calculations allow you to remove the unknown variable "b" from expressions;*
+ There is expression: |t2\*t0 - t1\*t1| = *u_*, which, according to number theory, gives a number that is a multiple of the number "m";
+ Using the "fad" function, all the numbers that are divisors of the number *u_* are found, since these numbers are potential values for the number "m";
+ We have an expression of the form: z = (a\*a\*x0) % u, where "u" is potential value of number "m"; For each potential value of the number "m", we are looking for such a number "z", which should be equal to x2;
+ 
