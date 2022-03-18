---
aliases: [""] 
tags: [Math DifferentialEquations] 
dateCreated: 2022-02-28 07:51:58
---
# Systems of Differential Equations
The process of breaking a differential equation 
into a system of equations.

$x_1' = F_1(x_1, x_2, \ldots, x_n, t)$
$x_2' = F_2(x_1, x_2, \ldots, x_n, t)$
$\vdots$
$x_n' = F_n(x_1, x_2, \ldots, x_n, t)$

With Initial Conditions:
$x_1(t_0) = x_1^0$ 
$\vdots$
$x_n(t_0) = x_n^0$ 
where $x_n^0$ signifies that it's the $0th$ term (initial condition) for $x_n$.

## Systems Existence and Uniqueness
### Linear 1st Order
See "Linear System of 1st Order Differential Equations" section of [[Existence and Uniqueness Theorems]].

### Non-Linear 1st Order
See "Non-Linear System of 1st Order Differential Equations" section of [[Existence and Uniqueness Theorems]].

*The Unique Solution Exists in some Interval $t_0 - h < t < t_0 + h$ inside $R$.*

## Example
$y'' + y' + 3y = 0; y(0) = 1, y'(0)=2$

Let $x_1 = y$ and $x_2 = y'$
$x_1' = y' = x_2$ and $x_2; = y'' = y'-3y = x_2 - 3x$

We can get the system of equations:
$$
\begin{align*}
	x_1' &= x_2\\
	x_2' &= -x_2 - 3x_1
\end{align*}
$$
Which we can rewrite into the Matrix:
$$
\overrightarrow{X} =
\begin{bmatrix}
	x_1 \\
	x_2
\end{bmatrix};
\overrightarrow{X'} = 
\begin{bmatrix}
	0 & 1 \\
	-3& -1
\end{bmatrix} \overrightarrow{X}
$$

