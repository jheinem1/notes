## Exponential Functions with General Bases

Let $b$ be a positive real number with $b\neq1$. Then for all real $x$,

$$
b^x=e^{x\ln{b}}\text.
$$

This definition fills in property 4 of Theorem 7.1 (see below).

![[mat266.natural-logarithm#^property_4]]

We use the definition of $b^x$ to write

$$
x^p=e^{p\ln{x}}\text{, for }x>0\text{ and }p\text{ real.}
$$

Taking the [[mat266.natural-logarithm]] of both sides and using the iverse relationship betweeen $e^x$ and $\ln{x}$, we find that

$$
lnx^p=ln{e^{p\ln{x}}}=p\ln{x}\text{, for }x>0\text{ and }p\text{ real.}
$$

## Derivatives and Integrals with Other Bases

Let $b>0$ and $b\neq1$. Then

$$
\frac{d}{dx}(\log_b{|u(x)|})=\frac{1}{\ln{b}}\frac{u\prime(x)}{u(x)}\text{, for }u(x)\neq0\text{ and }\frac{d}{dx}(b^{u(x)})=(\ln{b})b^{u(x)}u\prime(x)\text.
$$

For $b>0$ and $b\neq1$, $\int{b^x}{dx}=\frac{1}{\ln{b}}b^x+C$

## Example

![](/assets/images/2022-02-23-09-52-13.png)