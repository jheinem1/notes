
Geometric sums are finite sums in which each term is a constant multiple of the previous term. A geometric sum with $n$ terms has the form

$$
S_n=a+ar+ar^2+\cdots+ar^{n-1}=\sum_{k=0}^{n-1} ar^k\text,
$$

where $a\neq0$ and $r$ are real numbers. $r$ is called the ratio of the sum and $a$ is the first term of the series.

For example, the geometric sum with $r=0.1$, $a=0.9$, and $n=4$ is

$$
0.9+0.09+0.009+0.0009=0.9(1+0.1+0.00.001)=\sum_{k=0}^3 0.9(0.1^k)\text.
$$

## General formula

Assuming $r\neq1$ and solving for $S_n$, the general formula for the value of a geometric sum is

$$
S_n=a\frac{1-r^n}{1-r}\text.
$$

This is because to find the formula for the value of the geometric sum

$$
S_n=a+ar+ar^2+\cdots+ar^{n-1}=\sum_{k=0}^{n-1} ar^k\text,
$$

for any values of $a\neq0$, $r$, and the positive integer $n$, we can multiply both sides of the equation by the ratio $r$:

$$
rS_n=r(a+ar+ar^2+\cdots+ar^{n-1})=ar+ar^2+ar^3+\cdots+ar^{n-1}+ar^n\text.
$$

Subtracting the two sides leaves us with the general formula for the value of the geometric sum.