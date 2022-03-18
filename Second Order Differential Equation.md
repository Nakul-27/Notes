# Second Order Differential Equation
$\frac{d^2y}{dt^2} = f(f,y,\frac{dy}{dt})$
More Difficult and we can do **Only Linear Special Forms**

Requires 2 Initial conditions $y(t_0),y'(t_0)$.

If $y_1$ and $y_2$ that form a *fundamental set of solutions*, then the general solution is:
$y(t) = C_1y_1 + C_2 y_2$
We know a fundamental set if:
1. $y_1$ and $y_2$ satisfy the Differential Equation
2. $w \neq 0$ at some point $t$.

*Standard Form Linear: $P(t)y'' + Q(t)y' + R(t)y = G(t)$*

## [[Homogeneous]], Constant Coefficients
$P(t), Q(t), R(t)$ are all constants which make our differential equation: $ay'' + by' + cy = 0$.

$y = e^{rt}$ since when we take the derivative of $e$, it doesn't really change and then we can add $y'', y',$ and $y$ together like below:


$ar^2e^{rt} + bre^{rt} + ce^{rt} = 0$

$e^{rt}(ar^2+br+c) = 0$
And since $e^{rt}$ cannot be equal to 0, we get the [[Characteristic Equation]]:
$(ar^2+br+c)=0$.

$y = C_1e^{r_1t} + C_2e^{r_2t}$

*Behavior:* 
- Goes to positive/negative $\infty$ if *EITHER* $r_1, r_2 > 0$. 
- Goes to 0 if *BOTH* $r_1, r_2 < 0$.

Ex: $y'' + 2y' - 3y = 0$; $y(0) = 6$ and $y'(0) = 2$
Characteristic Equation: $r^2 + 2r - 3 = 0$
$r = -3, 1$

$y_1(t) = e^{-3t}$ and $y_2(t) = e^t$
$y_{1C}(t) = C_1e^{-3t}$ and $y_{2C}(t) = C_2e^t$
General Solution: 
$y(t) = C_1e^{-3t} + C_2e^t$
$y'(t) = -3C_1e^{-3t} + C_2e^t$

Using the Initial Conditions to solve for $C_1$ and $C_2$:

$6 = C_1 + C_2$
$-2 = -3C_1 + C_2$
$C_1 = 2, C_2 = 4$

$\therefore$ the Particular Solution is:
$y(t) = -2e^{-3t} + 4e^t$.

## Principle of [[Superposition]]
If $y_1$ and $y_2$ are solutions, then $c_1y_1 + c_2y_2$ is a solution. 
Given $y(t_0) = y_1, y'(t_0) = y'_0$ we can always find $c_1, c_2$ to satisfy $c_1y_1(t_0) + c_2y_2(t_0) = y_0$ and $c_1y_1'(t_0) + c_2y_2'(t_0) = y'_0$ 
$$
\begin{bmatrix}
y_1(t_0) & y_2(t_0) \\
y_1'(t_0) & y_2'(t_0)
\end{bmatrix}
\begin{bmatrix}
c_1 \\
c_2
\end{bmatrix}
=
\begin{bmatrix}
y_0 \\
y_0'
\end{bmatrix}
$$
Note that this can be expanded with to Matrices in [[Linear Algebra]] to include $n$ dimensions.

**[[Wronskian]]**: $W = y_1y_2' - y_2y_1'$

### Theorem 3.23
We can always find $c_1$ and $c_2$ to satisfy initial condition if and only if $w \neq 0$ at $t_0$.

### Theorem 3.24
Given $y_1$ and $y_2$ are solutions, $w(y_1,y_2) \neq 0$ at $t_0$, then $y = c_1y_1 + c_2y_2$ is the general solution.

Example
$t^2y'' - 2y = 0$
$y_1 = t^2$ and $y_2 = t^{-1}$
Both satisfy the differential equation.

$$
det
\begin{bmatrix}
t^2 & t^{-1} \\
2t & -t^2
\end{bmatrix}
= t^2(-t^{-2}) - (2t)(t^{-1}) = 3
$$
Therefore the general solution is of the form $y = c_1t^2 + c_2t^{-1}$.

### [[Abel's Theorem]]
if $y_2$ and $y_2$ are solutions to $y'' + p(t)y' + q(t)y = 0$ and $p,q$ are *continuous on $I$*, then:
$$
w(y_1,y_2) = Ce^{-∫p(t)dt}
$$
or
$$ W = det
\begin{bmatrix}
y_1 & y_2 \\
y_1' & y_2'
\end{bmatrix} = y_1y_2' - y_2y_1'
$$
Only $0$ when $C = 0$.

#### System of Linear Differential Equations

Given $\overset{\rightarrow}X^{(1)}$, $\overset{\rightarrow}X^{(2)}$, $\ldots$, $\overset{\rightarrow}X^{(n)}$ are solutions on $\overset{\rightarrow}{X}' = P(t)\overset{\rightarrow}{X}$ on $\alpha < t < \beta$.

Then:

$$
W
\begin{bmatrix}
\overset{\rightarrow}X^{(1)}, \overset{\rightarrow}X^{(2)}, \ldots, \overset{\rightarrow}X^{(n)}
\end{bmatrix}
$$
is either $0$ everywhere or nowhere on $\alpha < t < \beta$.

## Complex Roots
$ay'' + by' + cy = 0 \implies ar^2 + br + c = 0$

Roots: $r_1 = \lambda + \mu i$ and $r_2 = \lambda - \mu i$ lead to the general solution 
$$
y = C_1e^{(\lambda + \mu i)t} + C_2e^{(\lambda \mu i)t}
$$
$$
	y = e^{\lambda t}(C_1e^{\mu it} + C_2e^{-\mu i t})
$$
Euler's Formula
$$
e^{ix} = cos(x) + isin(x)
$$
*Behavior:*
![[Pasted image 20220202075100.png]]

Ex: $y'' + 9y = 0; y(0) = 0; y'(0) = 1$

Rewrite as $r^2 + 9 = 0$
$r = 3i,-3i$
$y(t) = e^{0t}(C_1cos3t + C_2sin3t)$
$0 = C_1cos(0) + C_2sin(0)$
$C_1 = 0$


$y'(t) = 3C_2cos(3t)$
$1 = 3C_2cos(0)$
$C_2 = \frac{1}{2}$

Therefore $y(t) = \frac{1}{3}sin3t$

## Repeated Roots

$(r+a)^2 = 0 \rightarrow r = -a \rightarrow y_1 = e^{-at}$ 
$r^2 + 2ar + a^2 = 0$
$y'' + 2ay' + a^2y = 0$

Using [[Abel's Theorem]]:
We can use Abel's Theorem
$$
W(y_1,y_2) = Ce^{-∫p(t)dt} \\
$$
$$W(y_1,y_2) = Ce^{-∫2adt} = Ce^{-2at}$$
And the Determinant definition of the Wronskian

$$
w(y_1,y_2) = \begin{bmatrix}
	e^{-at} & y_2 \\
	-ae^{-at} & y_2'
\end{bmatrix} = e^{-at}y_2' + ae^{-at}y_2
$$
Set them equal to each other
$$
\begin{align*}
	Ce^{-2at} &= y_2a^{-at} + y'e^{-at} \\
	y'_2e^{-at} + y_2e^{-at} &= Ce^{-2at} \\
	y'_2 +y_2a &= Ce^{at} \\
	\mu(t) = e^{∫adt} &= e^{at}
\end{align*}
$$

## [[Reduction of Order]]

## [[Undetermined Coefficients]]