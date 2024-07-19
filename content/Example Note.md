---
title: Ansatz Method
draft: false
---

*This is an example note for [[Fast Typesetting with Obsidian LaTeX Suite]]*.

>[!definition]+ Definition (Constant Coefficient ODE)
>A **Constant Coefficient ODE** is a second order equation of the form:
>
>$$
>ay'' + by' + cy = f(t)
>$$

>[!procedure]+ Procedure (Ansatz Method)
>The Ansatz Method is a way to find solutions to a constant coefficient ODE. For simplicity, assume $f(t) = 0$. If it isn't, use the method of undetermined coefficients. Take the **Ansatz** by letting $y(t) = e^{ rt }$:
>
>$$
>\begin{align}
>a\frac{\delta^2}{\delta^2t}e^{rt} + b\frac{\delta}{\delta t}e^{rt} + ce^{rt} &= 0 \\[5pt]
>ar^2e^{rt} + bre^{rt} + ce^{rt} &= 0 \\[5pt]
>e^{rt}(ar^2+br+c) &= 0
>\end{align}
>$$
>
>Since $e^{rt} \neq 0$, the ODE can only have a solution if $ar^2 + br +c = 0$. This is called the **Characteristic Equation** and its solutions are given by:
>
>$$
>r_1, r_2 = \frac{-b \pm \sqrt{b^2-4ac}}{2a}
>$$

>[!remark]+ Remark (Distinct Real Roots)
>If $r_{1}, r_{2} \in \mathbb{R}$ and $r_{1} \neq r_{2}$ the solution is:
>
>$$
>y(t) = c_{1}e^{ r_{1}t } + c_{2}e^{ r_{2}t }
>$$
>
>Alternatively, if $r_{1} = -r_{2}$, we can make a substitution to get:
>
>$$
>y(t) = A\cosh (r_{1}t) + B\sinh (r_{2}t) 
>$$

>[!remark]+ Remark (Repeated Real Roots)
>If $r_{1}, r_{2} \in \mathbb{R}$ and $r_{1} = r_{2}$ the solution is:
>
>$$
>y(t) = c_1e^{rt} + c_2te^{rt}
>$$

>[!remark]+ Remark (Complex Conjugate Roots)
>When $r_{1}, r_{2} \in \mathbb{C}$, the roots are complex conjugates of each other: $r_1 = \lambda + i\mu$, and $r_2 = \lambda - i\mu$. The values of $\lambda$ and $\mu$ are:
>
>$$
>\lambda = -\frac{b}{2a}, \quad\mu = \frac{\sqrt{4ac - b^2}}{2a}
>$$
>
>Euler's Identity gives us the general solution:
>
>$$
>y_h = C_1e^{\lambda t}\cos(\mu t) + C_2e^{\lambda t}\sin(\mu t)
>$$
