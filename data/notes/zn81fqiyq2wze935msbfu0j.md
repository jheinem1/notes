
Now that we know [[mat266.trigonometric-integrals.integrating-powers-of-sin-and-cos]], we can apply the half-angle formulas to integrate products of powers of sin and cos.

## Example

Evaluate the following integrals:

1. $\int{\sin^4{x}\cos^2{x}}\,dx$
2. $\int{\sin^3{x}\cos^{-2}{x}}\,dx$

### Solution

1. When both powers are even positive integers, the half-angle formulas can be used:
$$
\int{\sin^4{x}\cos^2{x}}\,dx=\int{(\frac{1-\cos{2x}}{2})^2(\frac{1+\cos{2x}}{2})^2}\,dx
$$
When expanded...
$$
=\frac18\int{(1-\cos{2x}-\cos^2{2x}+\cos^3{2x})}\,dx
$$
The third term in the integrand is rewritten with a half angle formula. For the last term, a factor of $\cos{2x}$ is written in terms of $\sin{2x}$ to prepare for a $u$-substitution:
$$
\int{\sin^4{x}\cos^2{x}}\,dx=\frac18\int{(1-cos{2x}-(\frac{1+\cos{4x}}{2})\,dx}+\frac18\int{(1-\sin^2{2x})\cos{2x}}\,dx
$$
Finally, the integrals are evaluated, using the substitution $u=\sin{2x}$ for the second integral. After simplification, we find that
$$
\int{\sin^4{x}\cos^2{x}}\,dx=\frac{1}{16}x-\frac{1}{64}\sin{4}-\frac{1}{48}\sin^3{2x}+C\text.
$$

2. When at least one power is odd, the following approach works:
$$
\int{\sin^3{x}\cos^{-2}{x}}\,dx=\int{sin^2{x}\cos^{-2}{x}\sin{x}}\,dx
$$
$$
=\int{(1-\cos^2{x})\cos^{-2}{x}\sin{x}}\,dx
$$
$$
=-\int{(1-u^2)u^{-2}}\,du
$$
$$
=\int{(1-u^{-2})}\,du=u+\frac1u+C
$$
$$
=\cos{x}+\sec{x}+C\text.
$$