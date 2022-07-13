
Assume $f$ and its first $n$ derivatives exist at $a$.

Our goal is to find an $n$th-degree polynomial that approximates the values of $f$ near $a$. The first step is to thse $p_2$ to obtain a cubic polynomial $p_3$ of the form

$$
p_3(x)=p_2(x)+c_3(x-a)^3
$$

that satisfies the four matching conditions

$$
p_3(a)=f(a)\text{, }p_3\prime(a)=f\prime(a),p_3\prime\prime(a)=f\prime\prime(a)\text{, and }p_3\prime\prime\prime(a)=f\prime\prime\prime(a)\text.
$$

Because $p_3$ is built "on top of" $p_2$, the first three conditions are met. The last condition, $p_3\prime\prime\prime(a)=f\prime\prime\prime(a)$, is used to determine $c_3$. A short calculation shows that $p_3\prime\prime\prime(a)=3*2c_3=3!c_3$, and so the last matching condition becomes $p_3\prime\prime\prime(a)=3!c_3=f\prime\prime\prime(a)$. Solving for $c_3$ gives $c_3=\frac{f\prime\prime\prime(a)}{3!}$. The cubic approximating polynomial is

$$
p_3(x)=f(a)+f\prime(a)(x-a)+\frac{f\prime\prime(a)}{2!}(x-a)^2+\frac{f\prime\prime\prime(a)}{3!}(x-a)^3\text.
$$