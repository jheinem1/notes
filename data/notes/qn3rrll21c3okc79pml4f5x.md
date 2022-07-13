
Suppose $f(x)=\frac{p(x)}{q(x)}$, where $p$ and $q$ are polynomials with no common factors and with the degree of $p$ less than the degree of $q$.

## Step 1

Factor the denominator $q$ in the form $(x-r_1)(x-r_2)\cdots(x-r_n)$, where $r_1,\cdots,r_n$ are distinct real numbers.

## Step 2

Form the partial fraction decomposition by writing
$$
\frac{p(x)}{q(x)}=\frac{A_1}{(x-r_1)}+\frac{A_2}{(x-r_2)}+\cdots+\frac{A_n}{(x-r_n)}
$$

## Step 3

Clear denominators by multiplying both sides of the equation in Step 2 by $q(x)=(x-r_1)(x-r_2)\cdots(x-r_n)$, which produces conditions for $A_1,\cdots,A_n$.

## Step 4

Solve for coefficients by equating like powers of $x$ in Step 3 to solve for the undetermined coefficients $A_1,\cdots,A_n$.

## Example

1. Find the partial fraction decomposition for $f(x)=\frac{3x^2+6x-2}{x^3-x^2-2x}$.

2. Evaluate $\int{f(x)}\,dx$.

### Solution

The partial fraction decomposition is done in five steps...

- Factor the denominator
$$
x^3-x^2-2x=x(x+1)(x-2)
$$
- Write the partial fraction decomposition
$$
\frac{3x^2+6x-2}{x^3-x^2-2x}=\frac{A}{x}+\frac{B}{x+1}+\frac{C}{x-2}
$$
(The goal is to find the undetermined coefficients $A$, $B$, and $C$.)
- Multiply both sides of the equation by $x(x+1)(x-2)$

$$
(\frac{A}{x}+\frac{B}{x+1}+\frac{C}{x-2})((x)(x+1)(x-2))
$$
$$
=(A+B+C)x^2-(A+2B-C)x-2A
$$

$$
(\frac{3x^2+6x-2}{x^3-x^2-2x})((x)(x+1)(x-2))
$$
$$
=(3)x^2+(6)x-(2)
$$

As you can see, the two sides of the equation can be grouped by the coefficients of $x^2$, $x^1$, and $x^0$.

- Solve for the coefficients of $x^2$, $x^1$, and $x^0$ on both sides of the equation
    - Equate coefficients of $x^2$: $A+B+C=3$
    - Equate coefficients of $x^1$: $-A-2B+C=7$
    - Equate coefficients of $x^0$: $-2A=-2$
- We can use the coefficients to find the values of $A$, $B$, and $C$ (e.g. $A=1$)
$$
f(x)=\frac{A}{x}+\frac{B}{x+1}+\frac{C}{x-2}
$$
$$
=\frac{1}{x}-\frac{2}{x+1}+\frac{4}{x-2}
$$

Now that we know $f(x)$, we can integrate it more easily.

$$
\int{\frac{3x^2+7x-2}{x^3-x^2-2x}}\,dx=\int{(\frac{1}{x}-\frac{2}{x+1}+\frac{4}{x-2})\,dx}
$$
$$
=\ln\frac{|x|(x-2)^4}{(x+1)^2}+C
$$