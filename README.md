# linear-congruential-generator-cracker

### This is my implementation of a program that finds the coefficients "a", "b" and "m" by four consecutive terms of a linear congruent sequence (x0, x1, x2, x3)

## What is LCS?

<img src="https://ie.wampi.ru/2022/09/23/IZOBRAZENIE_2022-09-23_122406181.png" alt="IZOBRAZENIE_2022-09-23_122406181.png" border="0">

+ LCS is a sequence of pseudorandom numbers obeying the law written above. According to the formula, it is possible to make a system of three equations for numbers from the condition.

## How it works?

+ Three pairwise differences of neighboring elements are made from a given sequence:
  + x1 - x0 = t0;
  + x2 - x1 = t1;
  + x3 - x2 = t2;
  + *These calculations allow you to remove the unknown variable "b" from expressions;*
+ There is expression: |t2\*t0 - t1\*t1| = *u_*, which, according to number theory, gives a number that is a multiple of the number "m";
+ Using the "fad" function, all the numbers that are divisors of the number *u_* are found, since these numbers are potential values for the number "m";
+ We have an expression of the form: z = (a\*a\*x0) % u, where "u" is potential value of number "m"; For each potential value of the number "m", we are looking for such a number "z", which should be equal to x2; If z = x2, then this is the potential value for the number "a";
+ Using the obtained values for "a" and "m", we will iterate over all possible values for the number "b", such that "b" < "m" (in order to iterate over the values of the residuals that the number "b" will give only once);
  + The values for "b" will be checked by a cycle in a system of three equations made up of the definition of LCS, bysubstitution; 
+ If the potential values for "a", "b" and "m" satisfy the system of equations, then these values will be output to the console, as well as the next value of the sequence x4 given by the condition.

## Example:

<img src="https://ie.wampi.ru/2022/09/23/IZOBRAZENIE_2022-09-23_123012044.png" alt="IZOBRAZENIE_2022-09-23_123012044.png" border="0">
