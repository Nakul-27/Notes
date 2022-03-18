# Series
Used to approximate a [[Second Order Differential Equation]] if we cannot find the solution

## General [[Power Series]]
$$
	\sum_{n = 0}^{\infty} a_n(x - x_0)^{n}
$$

## [[Taylor Series]]

$$
f(x) \ \sum_{n = 0}^{\infty} a_n(x - x_0)^{n} \text{ where } a_n = \frac{f^{(n)}(x_0)}{n!}
$$
Note that $f'(x) \sum_{n = 1}^{\infty}a_n \cdot n \cdot (x - x_0)^{n - 1}$
and: $f''(x) = \sum_{n = 2}^{\infty} \cdot  n \cdot (n - 1) \cdot (x - x_0)^{n - 2}$

## Testing Convergence
### Ratio Test
Ex: $\sum_{n = 1}^{\infty}\frac{n^2(x+2)^n}{3^n}$ 
Evaluate the Limit:
$$
\begin{align*}

&\lim_{x \to \infty}|\sum_{n = 1}^{\infty}\frac{n^2(x+2)^n}{3^n}| \\ 
&=|x+2|\lim_{x \to \infty}|\frac{n^2 + 2n + 1}{3n^2}| \\
&=|x + 2|\lim_{x \to \infty}|\frac{1 + 2/n + 1/n^2}{3}|\\
&=\frac{1}{3}|x + 2| < 1 \implies |x + 2| < 3
\end{align*}
$$
Therefore:
Radius of Convergence: $\rho = 3$
Interval of Convergence: $-5 < x < 1$

## Series Solutions
$y'' + p(x)y' + q(x)y = 0$
Ordinary Points: $x_0$ is ordinary if $p(x), g(x)$ are defined.
Singular Points: Points that aren't ordinary.

Ex: $y'' + x^2y + xy = 0$ around $x_0 = 0$
Assume that $y = \sum_{n=0}^{\infty}a_n\cdot x^n$
This means that $y' = \sum_{n=1}^{\infty}a_n \cdot n \cdot x^{n-1}$ and  $y'' = \sum_{n=2}^{\infty}a_n \cdot n \cdot (n-1) \cdot x^{n-2}$

$$
\begin{align*}
	\sum_{n=2}^{\infty}a_n \cdot n \cdot (n-1) \cdot x^{n-2} + x^2\sum_{n=1}^{\infty}a_n \cdot n \cdot x^{n-1} + x\sum_{n=0}^{\infty}a_n\cdot x^n &= 0\\
	
	\sum_{n=-1}^{\infty}a_{n+3} \cdot (n+3) \cdot (n+2) \cdot x^{n+1} + \sum_{n=1}^{\infty}a_n \cdot n \cdot x^{n+1} + \sum_{n=0}^{\infty}a_n\cdot x^{n+1} &= 0\\\\
	
	a_2(2)(1)x^0 + a_3(3)(2)x + \sum_{n=1}^{\infty}a_{n+3}(n+3)(n+2)x^{n+1} + \sum_{n=1}^{\infty}a_n \cdot n \cdot x^{n+1} + a_0x' + \sum_{n+1}^{\infty}a_nx^{n+1} &= 0 \\
	
	2a_2 + 6a_3x + a_0x + \sum_{n=1}^{\infty}x^{n+1}[a_{n+3}(n+3)(n+2) + a_nn + a_n] &= 0\\
	
\end{align*}
$$
Then solve for $a_2, a_3, a_0$:
$$
\begin{align*}
	2a_2 = 0 &\implies a_2 = 0 \\
	6a_3 + a_0 = 0 &\implies a_s = \frac{-1}{6}a_0 \\
	a_{n+3} &= \frac{-a_n(n+1)}{(n+3)(n+2)} \\
\end{align*}
$$
Which means that $a_5, a_8, a_{11}, \ldots$ will be 0, and the following will be true:
$a_0$ = Arbitrary
$a_1$ = Arbitrary
$a_2 = 0$
$a_3 = \frac{-1}{6}a_0$
$a_4 = \frac{-a_1(2)}{(4)(3)} = \frac{-1}{6}a_1$
$a_5 = 0$
$a_6 = \frac{-a_3(4)}{(6)(5)} = \frac{-2}{15}a_3 = \frac{1}{45}a_0$

$\therefore y = a_0 + a_1 - \frac{-1}{6}a_0x^3 - \frac{1}{6}a_1x^4 + \frac{1}{45}a_0x^6 \ldots$ 
