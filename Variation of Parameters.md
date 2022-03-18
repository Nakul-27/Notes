# Variation of Parameters
Used to solve a non-homogeneous [[Second Order Differential Equation]]

## Solve
$$U_1(t)' = \frac{-g(t)y_2}{W(y1,y2)} \implies U_1(t) = \int \frac{-g(t)y_2}{W(y_1,y_2)}$$
$$U_2(t)' = \frac{g(t)y_1}{W(y1,y2)} \implies U_2(t) = \int \frac{g(t)y_1}{W(y_1,y_2)}$$

## Steps
1. Find the complementary solution.
2. Assume $y_p$ is the complementary solution just multiplied by some arbitrary function and find $y'_p$ 
3. Require that all of the terms that have first derivatives add to 0.
4. Take $y''_p$ as the derivatives of the terms that don't add to 0.
5. Plug back into the original equation and cancel
6. Treat remaining (5) and (3) as 2 equations and solve for $U'_1(t)$ and $U'_2(t)$
7. Solve for $U_1(t)$ and $U_2(t)$

Ex: $y'' - 5y' +6y = 2e^t$
1.  $y_c = C_1e^{3t} + C_2e^{2t}$
2. $y_p = U_1(t)e^{3t} + U_2(t)e^{2t}$
	$y_p' = U_1'(t)e^{3t} + 3U_1(t)e^{3t} + U_2'(t)e^{2t} + 2U_2e^{2t}$
3. Require: $U_1'(t)e^{3t} + U_2'e^{2t} = 0$
4. $y''_p = 3U'_1(t)e^{3t} + 9U_1(t)e^{3t} + 2U'_2(t)e^{2t} + 4U_2(t)e^{2t}$
5. $$
	\begin{align*}
	&3U'_1(t)e^{3t} + 9U_1(t)e^{3t} + 2U'_2(t)e^{2t} + 4U_2(t)e^{2t}\\ &- 5(U_1'(t)e^{3t} + 3U_1(t)e^{3t} + U_2'(t)e^{2t} + 2U_2e^{2t})\\ &+ 6(U_1(t)e^{3t} + U_2(t)e^{2t})\\ &=
	2e^t
	\end{align*}
$$
6. $$
	\begin{align*}
	&3U'_t(t)e^{3t} + 2U'_2e^{2t} = 2e^t\\
	&U'_1(t)e^{3t} + U'_2(t)e^{2t} = 0
	\end{align*}
$$
7. $U_1(t) = e^{2t}$ and $U_2(t) = 2e^{-t}$ 
	Therefore our final solution is:
		$$
		y = C_1e^{3t}+C_2e^{2t} - e^{-2t}(e^{3t}) + 2e^{-t}(e^{2t})
	$$
	