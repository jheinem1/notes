
Simson's rule is a numerical method of integration, used to evaluate definite integrals. Usually to evaluate these integrals, the [[mat266.fundamental-theorem]] of calculus is used, however sometimes it can be too difficult to use by hand.

## Formula

$$
\int_a^b{f(x)}\,dx\approx S(n)=\frac{n}{3}(f(x_0)+4f(x_1))+2f(x_2)+\ldots+2f(x_{n-2})+4f(x_{n-1})+f(x_n))\text,
$$

where $n$ is the width of the interval, and $x_i$ is the $i$th point on the interval.

If using arrays, the integration can be performed with the following:

| $Y[n]$       | $D[n]$ |
| ------------ | ------ |
| $f(x_0)$     | 1      |
| $f(x_1)$     | 4      |
| $f(x_2)$     | 2      |
| $...$        | $...$  |
| $f(x_{n-2})$ | 2      |
| $f(x_{n-1})$ | 4      |
| $f(x_n)$     | 1      |

$n=\text{length of Y}$

$$
\int_a^b{f(x)}\,dx\approx S(n)=\frac{n}{3}\sum_{i=1}^{n}{(Y[i]*D[i])}
$$

This is generally easier when using a calculator, but either formula can be used.

## Example

[YouTube](https://youtu.be/7EqRRuh-5Lk)
