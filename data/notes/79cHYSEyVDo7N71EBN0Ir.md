
Suppose you are driving along a straight highway and your position relative to a reference point is $s(t)$ for times $t\geq0$. Your *displacement* over a time interval $[a,b]$ is the change in the position $s(b)-s(a)$.

If $s(b)>s(a)$, then your displacement is positive; when $s(b)<s(a)$, your displacement is negative.

![](/assets/images/2022-02-02-12-37-26.png)

Assuming $v(t)$ is the [[velocity|mat266.velocity]] of the object at a particular time ($t$), it follows that

$$
\int^b_a{v(t)}{dt}=\int^b_a{s\prime(t)}{dt}=s(b)-s(a)=\text{displacement}
$$

Therefore, the **displacement** of an object between $t=a$ and $t=b>a$ is

$$
s(b)-s(a)=\int^b_a{v(t)}{dt}
$$

($v(t)$ being the [[velocity|mat266.velocity]] of the object)

## Finding the displacement
To find the displacement of an object, we do not need to know its initial position. Whether an object moves from $s=-20$ to $s=-10$ or from $s=50$ to $s=60$ makes no difference- the displacement is 10 units.