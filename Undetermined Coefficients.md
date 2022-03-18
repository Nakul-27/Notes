# Undetermined Coefficients
Second Order Differential Equation, Linear Non-Homogeneous

Take the differential equation: $y'' + p(t)y' + q(t)y = g(t)$

## Theorem
Given any solution $Y_1$ and $Y_2$ to $y'' + p(t)y' + q(t) = g(t)$, then the fundamental solutions $y_1$ and $y_2$ to $y'' + p(t)y' + q(t)y = 0$ provide a general solution to the homogeneous equation $y = C_1y_1 + C_2y_2$.

Furthermore, then
$$
Y_1 - Y_2 = C_1y_1 + C_2y_2
$$

## Steps for Solving
1. Find the homogeneous solution
$$
y_c = C_1y_1 + C_2y_2
$$
2. Find a particular solution $y_p$
3. Combine with the general solution
$$
y = y_c + y_p
$$
![[Pasted image 20220204082814.png]]
Ex:
Solve $y'' - 2y' - 8y = 2t^2$
1. Find the Homogeneous solution
$$
\begin{align*}
r^2 - 2r - 8 &= 0 \\
(r-4)(r+2) &= 0 \\
r &= 4, -2 \\
\therefore y_c &= C_1e^{4t} + C_2e^{-2t}
\end{align*}
$$
2. Find $y_p$ Assuming a function in the form $g(t)$
$$
\begin{align*}
\text{ Assume } y_p &= A_0t^2 + A_1t + A_2\\
				y_p' &= 2A_0t + A_1 \\
				y_p'' &= 2A_0
\end{align*}
$$
Plugging in we get

$$
2A_0 - 2(2A_0 + A_1) + 8(A_0t^2 + A_1t + A_2) = 2t^2
$$
Which we can then simplify to get
$$
\begin{align*}
t^2: -8A_0 = 2 &\implies A_0 = \frac{-1}{4} \\
t: -4A_0 - 8A &\implies 1 - 8A_1 = 0 \implies A_1 = \frac{1}{8} \\
const: 2A_0 - 2A_1 - 8A_2 = 0 &\implies A_2 = \frac{-3}{32}
\end{align*}
$$
Therefore

$$
y_p = \frac{-1}{4}t^2 + \frac{1}{8}t - \frac{3}{32}
$$
3. General solution:
$$
y = C_1e^{4t} + C_2e^{-2t} - \frac{1}{4}t^2 + \frac{1}{8}t - \frac{3}{32}
$$
