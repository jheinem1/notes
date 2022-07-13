
Given a function such as
$$
f(x)\frac{1}{x-2}+2{x+4}\text,
$$
it is a straightforward task to find a common denominator and write the equivalent expression
$$
f(x)=\frac{3x}{x^2+2x-8}\text.
$$

The purpose of partial fractions is to reverse this process.

Rational Fraction | Partial Fraction Decomposition
| -- | -- |
$\frac{3x}{x^2+2x-8}$ | $\frac{1}{x-2}+\frac{2}{x+4}$
**Difficult to Integrate** | **Easy to Integrate**
$\int{\frac{3x}{x^2+2x-8}}\,dx$ | $\int{(\frac{1}{x-2}+\frac{2}{x+4})}\,dx$

## Methods

- [[mat266.partial-fractions.simple-linear-factors]]
- [[mat266.partial-fractions.repeated-linear-factors]]
- [[mat266.partial-fractions.irreducible-quadratic-factors]]

## Important When Integrating...

Keep in mind, $C\ln{(f(x))}=\int{\frac{C}{f(x)}}\,dx$, so

$$
\int{\frac{2}{x+4}+\frac{1}{x}-\frac{5}{x}}=2\ln{(x+4)}+\ln{(x)}-5\ln{(x)}
$$