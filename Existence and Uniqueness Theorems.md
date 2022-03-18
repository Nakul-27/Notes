# Existence and Uniqueness Theorems
## Linear 1st Order
Theorem 2.4.1 in **Boyce and DiPrima** #textbook 

$y' + p(t)y = g(t), y(t_0)=y_0$
Conditions: (Need to be in standard form) *all* $p(t)$ and $g(t)$ are continuous on some interval $\alpha < t < \beta$ that contains $t$.

Then $\exists$ a unique solution to the [[Initial Value Problem]]

Example: 
$y' + \frac{1}{t-1}y = ln(t), y(2) = 0$
$p(t) = \frac{1}{t-1}, g(t) = ln(t)$
Discontinuity at $t = 1$ for $p(t)$ and $t \leq 0$ for $g(t)$.
*Since $y(2) = 0$, then we know that a unique solution exists within the Interval $(1, \infty)$.*

## Non-Linear 1st Order
Theorem 2.4.2 in Boyce and DiPrima #textbook 
**Cannot Always solve a Non-Linear Differential Equation**

$y' = f(t,y)$
Conditions: $f(t,y)$ and $\frac{\partial f}{\partial y}$ are continuous on some rectangle $P$. $\alpha < t < \beta$, $\gamma < y < \delta$ containing $t_0$ and $y$.

Then $\exists$ a unique solution for some interval $t$ *within* $\alpha < t < \beta$.

Example:
$y' = 2ty^2$ 
$f(t,y) = 2ty^2$ (continuous everywhere)
$\frac{\partial f}{\partial y} = 4ty$ (continuous everywhere)

$\int \frac{1}{y^2}dy = \int 2t dt$ 
$-\frac{1}{y} = t^2 + C$ 
$y(t) = \frac{-1}{t^2 + C}$ (Depending on $t$ and $C$ there exists someplace where the function is not defined)

We can use the method of [[Successive Approximation]] to attempt to get closer to a solution

## Linear 2nd Order
$y'' + p(t)y' + q(t)y = g(t)$
Given that $p(t), q(t), g(t)$ are continuous on an interval, $I$ , containing the initial condition, *$\exists$  unique solution exists on $I$*.

## Linear System of 1st Order Differential Equations 
Use [[Linear Algebra]]
The following conditions must be satisfied:
1. $p_{11}(t), \ldots, p_{nn}(t)$
2. $g_1(t), \ldots, g_n(t)$
Continuous on an Interval $\alpha < t < \beta$. 

Given $\overset{\rightarrow}{X^{(1)}}$,  $\overset{\rightarrow}{X^{(2)}}$, $\ldots$,  $\overset{\rightarrow}{X^{(n)}}$ are solutions on $\alpha < t < \beta$ are linearly independent on each point in $\alpha < t < \beta$.
Then $\overset{\rightarrow}{X^{(1)}}$,  $\overset{\rightarrow}{X^{(2)}}$, $\ldots$,  $\overset{\rightarrow}{X^{(n)}}$ is a fundamental set of solutions known as the **General Solution.** 

Given
$$ X(t) =
\begin{bmatrix}
\overset{\rightarrow}{X^{(1)}} \vdots \overset{\rightarrow}{X^{(2)}} \vdots \cdots \vdots \overset{\rightarrow}{X^{(n)}} 
\end{bmatrix}
$$
$det(X(t)) = W(\overset{\rightarrow}{X^{(1)}}, \overset{\rightarrow}{X^{(2)}}, \ldots, \overset{\rightarrow}{X^{(n)}})$ where $W$ refers to the [[Wronskian]]. 

If $det(X(t)) \not= 0$ at every point in $\alpha < t < \beta$, then $X(t)$ is a solution.

## Non-Linear System of 1st Order Differential Equations
The following conditions must be satisfied:
1. $F_1, F_2, \ldots, F_n$ have to be continuous on some region $R$. 
2. $\frac{\partial F_1}{x_1}...\frac{\partial F_1}{x_n}$ 
	$\vdots$
	$\frac{\partial F_n}{x_1}...\frac{\partial F_n}{x_n}$ 
3. Initial condition must be in $R$. 

A Unique Solution Exists

