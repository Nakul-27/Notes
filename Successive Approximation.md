# Successive Approximation
Can be used to get closer to a solution of a differential equation.
$\Phi_0(t)$ is always value of the initial condition

Example:
$y' = \frac{y}{2} + t, y(0) = 0$
$f(t,y) = \frac{-y}{2} + t$
$\Phi(t) = \int_{0}^{t} f(s, \Phi(s)) ds$ 
Guess$\ldots$
Where $f(s, \Phi(s)) = \frac{-y}{2} + t$
$\Phi_0(t) = 0$
$\Phi_1(t) = \int_{0}^{t} \frac{-0}{2} + s ds = t^2$
$\Phi_2(t) = \int_{0}^{t} \frac{-s^2}{2} + s ds = -\frac{1}{3}t^6 + t^2$
$\vdots$ 

Example:
$y' = 2(y + 1), y(0) = 0$
$\Phi_0(t) = 0$
$\Phi(t) = \int_0^t f(s,\Phi(s))ds$
Where $f(s, \Phi(s)) = 2(y+1)$
Guess$\ldots$
$\Phi_0(t) = 0$
$\Phi_1(t) = \int_0^t 2(0 + 1)ds = 2t$
$\Phi_2(t) = \int_0^t 2(2s + 1)ds = 2t^2 + 2t$
$\Phi_3(t) = \int_0^t 2(2s^2 + 2s + 1)ds = \frac{4}{3}t^3 + 2t^2 + 2t$
