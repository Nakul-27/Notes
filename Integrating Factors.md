# Integrating Factors
## Want to take the left hand side and turn it into something that we can take the [[derivative]] of.
Example:

$(t^2y)' = cost$

$\int{\frac{d(t^2y)}{dt}}dt = \int{cos(t)}dt$

$t^2y = sin(t) + C$

$t^2y' + 2ty = cos(t)$
Want the outcome of a [[Product Rule]].

[[Leibniz]] discovered that we can multiply multiply any linear first order Differential Equations by some function $\mu(t)$ (Different from [[Leibniz Method for Integration]])

### Method
**General Solution**:
$y' + p(t)y = g(t)$

Propose $\mu(t)$
$\mu(t)y' + \mu(t)p(t)y = \mu(t)g(t)$

$(\mu(t)y)' = \mu(t)g(t)$
$\mu(t)y = \int\mu(t)g(t)dt + C$
$y(t) = \frac{1}{\mu(t)}\int_{t_0}^{t}\mu(s)g(s)ds + C$

Want: $\frac{d\mu}{dt} = \mu(t) p(t)$

$\int{\frac{1}{\mu(t)}}d\mu = \int{p(t)}dt$

$ln|\mu (t)| = \int{p(t)}dt$
Need to leave $p(t)$ as an integral since it's a function and not a constant value.


$\mu(t) = Ce^{\int{p(t)}dt}$

### Example from the General:
$y' + \frac{1}{t}y = t^2$
where $p(t) = \frac{1}{t}$ and $y(t) = t^2$

$\mu(t) = Ce^{\int{\frac{1}{t}}dt} = e^{ln(t)} = t$
$ty' + t(\frac{1}{t})y = t^3$
$ty' + y = t^3$
$(ty)' = t^3$
$ty = \int{t^3}dt$
$ty = \frac{1}{4}t^4 + C$
$y = \frac{1}{4}t^3 + \frac{C}{t}$
$y = \frac{1}{4}t^3 + C$

### Another Example: 
$y' - 2y = t^2e^{2t}$

$p(t) = -2$ and $g(t) = t^2e^{2t}$

$\mu(t) = e^{\int-2dt} = e^{-2t}$

$e^{-2t}y' - 2e^{-2t}y = t^2$
$\mu(t)y' = (e^{-2t}y)' = t^2$

$e^{-2t}y = \int t^2 dt$

$e^{-2t}y = \frac{1}{3}t^3 + C$

$y = \frac{1}{3}t^3e^{2t} + Ce^{2t}$
