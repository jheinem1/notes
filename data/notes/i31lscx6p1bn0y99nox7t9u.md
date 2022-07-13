
A *simple* factor is raised to the first power, however a *repeated* factor is raised to a power higher than the first power.

Suppose $(x-r)^m$ appears in the denominator, where $m>1$ is an integer. Then there must be a partial fraction for each power of $(x-r)$ up to and including the $m$th power. For example, if $x^2(x-3)^4$ appears in the denominator, then the partial fraction decomposition includes the 6 terms
$$
\frac{A}{x}+\frac{B}{x^2}+\frac{C}{x-3}+\frac{D}{(x-3)^2}+\frac{E}{(x-3)^3}+\frac{F}{(x-3)^4}\text.
$$

The [[rest of the procedure|mat266.partial-fractions.simple-linear-factors]] remains the same, though the amount of work increases with the number of coefficients.

## Procedure

Suppose the repeated linear factor $(x-r)^m$ appears in the denominator of a proper rational function in reduced form.

The partial fraction decomposition has a partial fraction for each power of $(x-r)$ up to and including the $m$th power; that is, the partial fraction decomposition contains the sum
$$
\frac{A_1}{(x-r)}+\frac{A_2}{(x-r)^2}+\frac{A_3}{(x-r)^3}+\cdots+\frac{A_m}{(x-r)^m}\text,
$$
where $A_1,\ldots,A_m$ are constants to be determined.