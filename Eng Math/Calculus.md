# Calculus
## Types : 
- Algebraic and Vector
- Both alg and vector has 2 main operations 
    - Differentiation
    - Integration

---
## Pre-requisites 
- Functions
1. Parabolas : (open up, down, left and right)
2. Mod x : (v shaped graph)
- SHIFT FUNCTIONS with vertex at (h,k)
`y = f(x) => (y-k) = f(x-h)`

## LIMIT, Continuity, Differentiability
- ***LIMIT*** 
    - Limit at x=a exists if `LHL = RHL`
- ***Continuity*** 
    - A Function f(x) is continuous at x=a if 
    `Limit of f at x=a = f(a)`
    - `LHL = RHL = f(a)`
- ***Differentiable*** 
    - Function should be continuous
    - LH derivative = RH derivative
### NOTE
- All differentiable functions are continuous
- All continuous function are not necessarily differentiable. 
- Eg: `y=|x| is continuous everywhere but not differentiable at x=0`
- If a function is defined, the value should be finite but not infinity
- NOTATIONS: 

```
LHL = f(a-0) = lt h->0 f(a-h)
RHL = f(a+0) = lt h->0 f(a+h)
```
-----------
## L'Hopital Rule 
- for finding limits of indeterminate forms like 0/0, inf/inf, 0 x inf, inf - inf, inf <sup>0</sup>, 0 <sup>0</sup>, 1<sup>inf</sup>


![image](https://user-images.githubusercontent.com/43994542/148759954-d8d4ace1-dd2a-4b94-b8ee-8c8d2df2b144.png)


---
## MEAN VALUE THEOREM
```
For a given planar arc between two endpoints, 
there is at least one point at which 
the tangent to the arc is parallel to the secant through its endpoints.
```
Let f be continuous on a closed interval [a, b] and differentiable on the open interval (a, b). Then there is at least one point c in (a, b) where

`f '(c) = (f(b) - f(a)) / (b - a)`

## ROLLE's Theorem
Let f be continuous on a closed interval [a, b] and differentiable on the open interval (a, b). 
If `f(a) = f(b)`, then there is at least one point c in (a, b) where `f '(c) = 0`.

---
## SERIES EXPANSION
1.  e<sup>x</sup>  = 1 + x/1! + x<sup>2</sup>/2! + ...
1.  e<sup>-x</sup>  = 1 - x/1! + x<sup>2</sup>/2! + ...
1.  sinx  = x - x<sup>3</sup>/3! +  x<sup>5</sup>/5!...
1.  cosx  = 1 - x<sup>2</sup>/2! +  x<sup>4</sup>/4!...
1.  sinhx  = x + x<sup>3</sup>/3! +  x<sup>5</sup>/5!... = (e<sup>x</sup> - e<sup>-x</sup>)/2
1.  coshx  = 1 + x<sup>2</sup>/2! +  x<sup>4</sup>/4!... = (e<sup>x</sup> + e<sup>-x</sup>)/2


---
## INTEGRATION
- ODD FUNCTION 
    - `f(x) = -f(-x)` and symmetric about origin
- EVEN FUNCTION
    - `f(x) = f(-x)` and symmetric about y axis
- If limit is from -a to +a, Integral can be simplified (ODD FUNCTION -> 0 and EVEN function -> 2 times Integral from limit 0 to +a)




