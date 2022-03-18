# Separation of Variables
## Used for a special case of First Order Differential Equations (When the Diff Eq is Non-Linear and Separable)

### Example:
$\frac{dy}{dx} = \frac{x}{y}$

$\int y dy = \int x dx$ 

$\frac{1}{2}y^2 = \frac{1}{2}x^2 + C$

$y = \pm \sqrt{x^2 + C}$

### Another Example:
$\frac{dy}{dx} = (1-2x)y^2, y(0) = \frac{1}{6}$
$\int \frac{1}{y}dy = \int(1-2x)dx$
$-\frac{1}{y}=x-x^2+C$
General Solution: $y = \frac{-1}{x-x^2+C}$
$-\frac{1}{6} = \frac{-1}{0-0^2+C} \implies C = 6$
Particular Solution: $y(x) = \frac{-1}{x-x^2+6}$

$y(x)$ is undefined at $x = -2$ and $x = 3$.

We are given that $y(0) = -\frac{1}{6}$.

$\therefore$ we know that the [[Interval of Validity]] is $(-2, 3)$.


**Justification Using the [[Chain Rule]]:**
$N(y) * \frac{dy}{dx} = M(x)$ where $N(y) = \frac{df}{dy}$
$\frac{df}{dx} = M(x)$
$\int{\frac{df}{dx}}dx = \int{M(x)dx}$
$f(y(x)) = \int{M(x)dx}$

**AND**

$\int{\frac{df}{dy}dy} = \int{N(y)dy}$
$f(y(x)) = \int{N(y)dy}$

$\therefore \int{N(y)dy} = \int{M(x)dx}$

