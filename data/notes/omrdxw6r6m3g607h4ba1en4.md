
## Reduction formulas

Assume $n$ is a positive integer.

1. $\int{\sin^n{x}}\,dx=-\frac{\sin^{n-1}{x}\cos{x}}{n}+\frac{n-1}{n}\int{\sin^{n-2}{x}}\,dx$
2. $\int{\cos^n{x}}\,dx=\frac{\cos^{n-1}{x}\sin{x}}{n}+\frac{n-1}{n}\int{\cos^{n-2}{x}}\,dx$
3. $\int{\tan^n{x}}\,dx=\frac{\tan^{n-1}{x}}{n-1}-\int{\tan^{n-1}{x}}\,dx$, $n\neq1$
4. $\int{\sec^n{x}}\,dx=\frac{sec^{n-2}{x}\tan{x}}{n-1}+\frac{n-2}{n-1}\int{sec^{n-2}{x}}\,dx$, $n\neq1$

## Example

Evaluate $\int{\tan^4{x}}\,dx$.

### Solution

Reduction formula 3 gives
$$
\int{tan^4{x}}\,dx=\frac13\tan^3{x}-\int{tan^2{x}}\,dx
$$
$$
=\frac13\tan^3{x}-(\tan{x}-\int{\tan^0{x}}\,dx)
$$
$$
=\frac13\tan^3{x}-\tan{x}+x+C\text.
$$

An alternative solution uses the identity $tan^2{x}=sec^2{x}-1$:
$$
\int{\tan^4{x}}\,dx=\int{\tan^2{x}(\sec^2{x}-1)}\,dx
$$
$$
=\int{\tan^2{x}(\sec^2{x}-1)}\,dx-\int{\tan^2{x}}\,dx
$$

The substitution $u=\tan{x}$, $du=\sec^2{x}$ is used in the first integral, while the identity $\tan^2{x}=sec^2{x}-1$ is used in the second integral:
$$
\int{tan^4{x}}\,dx=\int{\tan^2{x}\sec^2{x}}\,dx-\int{\tan^2{x}}\,dx
$$
$$
=\int{u^2}\,du-\int{(\sec^2{x}-1)}\,dx
$$
$$
=\frac{u^3}{3}-\tan{x}+x+C
$$
$$
=\frac13\tan^3{x}-\tan{x}+x+C\text.
$$