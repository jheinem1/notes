
A differential equation involved an unknown function $y$ and its derivatives. The unknown in a differential equation is not a number, but rather a function.

Some examples of differential equations include...

-
$$
\frac{dy}{dx}+4y=\cos{x}
$$
-
$$
\frac{d^2y}{dx^2}+16y=0
$$
-
$$
y'(t)=0.1y(100-y)
$$

$x$ ant $t$ are commonly used as the independent variables ($t$ is generally used for time-dependent problems).

## Goal

The purpose of solving a differential equation is to find the function $y$ that satisfies the differential equation.

For example, if substituting $y=\cos{4x}$ and $y''=-16\cos{4x}=0$ into the second equation above, we get...

$$
-16\cos{4x}+16\cos{4x}=0\text,
$$

with $y=\cos{4x}$ reflected on the **righthand** side of the $+$ sign and $y''=-16\cos{4x}$ reflected on the **lefthand** side of the $+$ sign. This implies that $y=\cos{4x}$ is a solution to the differential equation.

## Terminology

The general **first-order linear differential equation** has the form

$$
\frac{dy}{dt}+p(t)y=q(t)\text,
$$

where $p$ and $q$ are given functions of $t$. This equation is linear because $y$ and $y'$ appear to the first power and not in products or compositions involving $y$ or $y'$.

### Order

The order of a differential equation is the highest order that appears on a derivative in the equation.

Of the three examples, the first two are **first order**, and the third is **second order**.

### Linear

A differential equation is linear if the unknown function $y$ and its derivatives appear only to the first power and are not composed with other functions. A linear equation also cannot have products or quotients of $y$ and its derivatives.

Of the examples, the first two are **linear**, and the third is **nonlinear** (because the right side contains $y^2$).

A linear differential equation *cannot* have terms such as $y^2$, $yy'$, or $\sin{y}$, where $y$ is the unknown function.

## General Solution

Differential equations can be solved through integration. You must "undo" the derivative $y'(t)$ in order to find $y$.

The most general solution of a first-order differential equation involves **one** arbitrary constant, whereas a second-order differential equation requires **two** arbitrary constants. This carries onto equations of $n$th order, where they have $n$ arbitrary constants.

### Initial Conditions

A differential equation is often accompanied by initial conditions that specify the values of $y$ and possibly $y'$ at the start of the problem.

In general, a differential equation of the $n$th order requires $n$ initial conditions, which are used to determine the $n$ arbitrary constants in the general solution.

A differential equation with the appropriate initial conditions is called an **initial value problem**. A first-order initial value problem generally has the form

$$
\begin{matrix}
y'(t)=F(t,y)&\text{Differential equation}\\
y(a)=b\text,&\text{Initial condition}
\end{matrix}
$$

where $a$ and $b$ are the initial values, and $F$ is a given expression that involves $t$ and/or $y$. A solution to this problem is a function $y(t)$ that satisifies the differential equation on an interval $I$ and whose graph includes the point $(a,b)$. $I$ is called the **domain** of the solution.

### Verifying Solutions

To verify a solution to a differential equation, we can use substitution to prove that a function $y(t)$ satisfies the differential equation $y'(t)=F(t,y)$.

To prove $y(t)=Ce^{2.5t}$ is a solution to the equation $y'(t)=2.5y(t)$ (where $C$ is an arbitrary constant), we differentiate $y(t)=Ce^{2.5t}$ to get $y'(t)=2.5Ce^{2.5t}$.

$$
y'(t)=2.5Ce^{2.5t}=2.5Ce^{2.5t}=2.5y(t)
$$

This means that the function $y(t)$ satisfies the equation $y'(t)$ for any value of $C$. From this, we know that $y(t)$ is a family of solutions of the differential equation.

## Solving

[solving-differential-equations.pdf](https://github.com/jheinem1/notes/tree/main/vault/assets/solving-differential-equations.pdf)