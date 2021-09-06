# Golfing Expressions
[Source](https://codegolf.stackexchange.com/questions/223581/golfing-expressions)

We can write mathematical expressions using the standard math operators (,),+,*,/,- available pretty much universally. We allow the symbols a, b, c, d and integers (e.g. 1, 45, etc.) but will restrict to just these four symbols. (Bonus points if you can handle more.) The goal is to take an expression as input and output a shorter expression that is mathematically equivalent to the input.

Edit: implicit multiplication such as 2a is not valid. It should be 2*a.

[To make this a bit easier, we will only ever divide by integers, and never the symbols. In other words, an expression is a polynomial in 4 variables with rational coefficients.]

## Examples
```
input  1: 1+1/2  (5 characters)
output 1: 3/2    (3 characters)

input  2: a*(1-b)*(1+b)  (13 characters)
output 2: a-a*b*b        (7 characters)

input  3: a*b*2/7-a*b*b/7  (15 characters)
output 3: a*b*(2-b)/7      (11 characters)

input  4: b*c*c+2*a*c*d-2*a*c-2*b*c-c*c-2*a*d-2*c*d+4*c+2*d  (49 characters)
output 4: c*(b*c-2*a-2*b-c+4)+2*d*(1-a)*(1-c)                (35 characters)

input  5: a*c+b*c+a*d+b*d+3*a+3*b+c+d+4  (29 characters)
output 5: (1+a+b)*(3+c+d)+1              (17 characters)
```

## Scoring
Shortest (valid) output wins. As a result, whoever has the shortest total (valid) output from the 20 randomly generated expressions is the winner. I will also verify that the winning solution actually works by creating 20 more, similar expressions and testing those.

There is a shortest solution in each case, so if multiple people come up with a solution that finds the shortest answer for every input, and not just the ones below, whoever got it first wins.

## "Random" Inputs
```
(2*a*a*a-2*a*a*d+2*b*d*d+d*d*d-2*a*a+2*a*b-b*c-a*d+b*d+a+c)/2
(-d*d*d+2*c+d)/2
-b*c*c-2*a*c*d+2*a*c+2*b*c+2*a*d
2*a*a*c+2*a*c*d-2*c*d*d-2*b*b+2*a*c+2*b*c-2*c*d-2*d*d-2*a-b+2*c+d+1
-b*c*c-2*a*c*d+c*c+2*c*d+2*a+b
(-2*a*a*b*b+a*a*a*c+b*c*c*d+2*c*d*d*d-d*d*d-2*a*c+2*b*c+2*c*c+d*d)/3
(-2*a*a+b*c-2*b*d+2*a-2*b-1)/2
(b*b*c+a*c*c-2*b*d*d-c*d*d-a*a-2*a*b-b*b-a*c+c*c+2*a*d-b*d-2*d*d)/4
(a*a+b*d-c*d-c-2*d)/2
-a*a+2*a*b+2*b*b+2*a*c-a*d-2
-b*c*c-2*a*c*d+2*a+b
(a*b*b+2*a*b*c-b*c*c-a*d*d-b*b+a*c+b*c-c*c+2*a*d+a+2*b+d)/4
(-8*a*b*c-4*a*a*d+4*a*a+8*a*b+4*a*c+4*b*c+4*a*d-8*a-4*b+3)/3
(-2*a*a*a*a+c*c*c*c-a*b*c*d+2*b*b*c*d-a*c*c*d-2*c*c*c*d+a*a-2*b*b+2*a*c+a*d)/3
b*c*c+2*a*c*d-2*a*c-2*b*c-c*c-2*a*d-2*c*d+4*c+2*d
(-2*a*b*b*b+c*c*c*c-2*a*a)/3
```
