# Reduction of Order
You have to know one solution $y_1$ and want to find a second $y_2 = v(t)y$.

For [[Second Order Differential Equation]] that are Linear and Homogeneous.
$y'' + p(t)y' + q(t)y = 0$
But we need one solution $y_1$.

Assume that $y_2 = v(t)y_1$ 
Substitute $y_2$ into the DE.

Then $w = v'$.

Ex: $t^2y'' + 3ty' + y = 0; y(1) = t^{-1}$
Assume 
$$
\begin{align*}
	y_2 &= v(t)t^{-1} \\\\
	y'_2 &= -v(t)t^{-2} + v'(t)t^{-1} \\\\
	y''_2 &= 2vt^{-3} -v'(t)t^{-2} + v''(t)t^{-1} - v't^{-2}
\end{align*}
$$  Plug back in
$$
	\begin{align*}
		t^2(v''(t)t^{-1} - 2v'(t)t^{-2} + 2vt^{-3}) &+ \\\\
		3t(-vt^{-2} + v'(t)t^{-1}) &+\\\\
		(v(t)t^{-1}) &= 0
	\end{align*}
$$
Simplify

$$
\begin{align*}
	tv(t)'' - 2v(t)' &+\\\\
	\frac{2}{t}v(t) &- \frac{3}{t}v(t) +\\\\
	3v'(t) &+ \frac{1}{t}v(t) = 0
\end{align*}
$$

