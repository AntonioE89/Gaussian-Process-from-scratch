# Gaussian-Process-from-scratch

In this notebook we construct a Gaussian process from scratch, using only numpy and scipy packages. This is for educational purposes, and although it has a modest performance it is not build for speed. 

## 1D input 1D output example

For example, we model f(x):=sin(x) + N(0,10^-3)

We gather 4 samples:

X = [-4,-1,1,2]

and then have 

Y = [sin(-4), sin(-1), sin(1), sin(2)] + N(0,10^-3)

![image](https://user-images.githubusercontent.com/6797764/112169902-841c7e00-8bea-11eb-9c8d-c69b29d90307.png)

## 2D input 1D output example

$
X =
\begin{bmatrix}
    x^1_1 & x^1_2 \\
    x^2_1 & x^2_2\\
     \vdots\\
    x^n_1 & x^n_2 
\end{bmatrix}\qquad$ 
and 
$\qquad Y =
\begin{bmatrix}
    \text{sin}(x^1_1 + x^1_2)+\epsilon\\
    \text{sin}(x^2_1 + x^2_2)+\epsilon\\
    \vdots\\\\
    \text{sin}(x^n_1 + x^n_2)+\epsilon
\end{bmatrix}$

where $f({\bf x}):=\text{sin}(x^1+x^2)$, and $\epsilon \sim \mathcal{N}(0,10^{-3})$

![image](https://user-images.githubusercontent.com/6797764/112172447-a2837900-8bec-11eb-84d6-d00faf50a16a.png)
