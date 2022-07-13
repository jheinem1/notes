
## Integrals involving $a^2-x^2$

Suppose you are faced with an integral whose integrand contains the term $a^2-x^2$, where $a$ is a positive constant. Observe what happens when $x$ is replaced with $a\sin{\theta}$:

(Replace $x$ with $a\sin{\theta}$)
$$
a^2-x^2=a^2-(a\sin{\theta})^2
$$
(Simplify)
$$
=a^2-a^2\sin^2{\theta}
$$
(Factor)
$$
a^2(1-\sin^2{\theta})
$$
($1-sin^2{\theta}=\cos^2{\theta}$)
$$
=a^2\cos^2{\theta}\text.
$$

### Example: Area of a circle

Verify area of a circle of radius $a$ is $\pi a^2$.

#### Solution

The function $f(x)=\sqrt{a^2-x^2}$ describes the upper half of a circle centered at the origin with radius $a$.

![](/assets/images/2022-03-02-12-57-05.png)

The region under this curve on the interval $[0,a]$ is a quarter-circle. Therefore, the area of a full circle is
$$
4\int_0^a{\sqrt{a^2-x^2}}\,dx\text.
$$

### Example: Sine substitution

Evaluate $\int{\frac{1}{(16-x^2)^{\frac32}}\,dx}$.

#### Solution

The factor $16-x^2$ has the for $a^2-x^2$ with $a=4$, so we can use the substitution $x=4\sin{\theta}$ to evaluate the integral.

It follows that $dx=4\cos{\theta}\,d\theta$. We now simplify $(16-x^2)^{\frac32}$:

(Substitute $x=4\sin{\theta}$)
$$
(16-x^2)^{\frac32}=(16-(4\sin{\theta})^2)^{\frac32}
$$
(Factor)
$$
=(16(1-\sin^2{\theta}))^{\frac32}
$$
($1-\sin^2{\theta}=\cos^2{\theta}$)
$$
=(16\cos^2{\theta})^{\frac32}
$$
(Simplify)
$$
=64\cos^3{\theta}\text.
$$

Replacing the factors $(16-x^2)^{\frac32}$ and $dx$ of the original integral with appropriate expressions in $\theta$ yields:

$$
\int{\frac{dx}{(16-x^2)^{\frac32}}}=\int{\frac{4\cos{\theta}}{64\cos^3{\theta}}}\,d\theta
$$
(Simplify)
$$
=\frac{1}{16}\int{\sec^2{\theta}}\,d\theta
$$
(Evaluate the integral)
$$
=\frac{1}{16}\tan{\theta}+C\text.
$$

The final step is to express this result in terms of $x$.

We can do this using a reference triangle showing the relationship between $x$ and $\theta$:

![](/assets/images/2022-03-02-13-08-57.png)
$$
\sin{\theta}=\frac{x}{4}
$$
$$
\tan{\theta}=\frac{x}{\sqrt{16-x^2}}
$$

Using this triangle, we see that $\tan{\theta}=\frac{x}{\sqrt{16-x^2}}$. This implies that

$$
\int{\frac{dx}{(16-x^2)^{\frac32}}}=\frac{1}{16}\tan{\theta}+C=\frac{x}{16\sqrt{16-x^2}}+C
$$

## Integrals involving $a^2+x^2$ or $x^2-a^2$

Contains... | Corresponding Substitution | Useful Identity
--- | --- | ---
$a^2-x^2$ | $x=a\sin{\theta}$, $\frac{\pi}{2}\leq\theta\leq\frac{\pi}{2}$ | $a^2-a^2\sin^2{\theta}=a^2\cos^2{\theta}$
$a^2+x^2$ | $x=a\tan{\theta}$, $-\frac{\pi}{2}\leq\theta\leq\frac{\pi}{2}$ | $a^2+a^2\tan^2{\theta}=a^2\sec^2{\theta}$
$x^2-a^2$ | $x=a\sec{\theta}$, $\begin{cases} 0\leq\theta\leq\frac{\pi}{2}&\text{for }x\geq a\\\frac{\pi}{2}<\theta\leq\pi&\text{for }x\leq-a\end{cases}$ | $a^2\sec^2{\theta}-a^2=a^2\tan^2{\theta}$