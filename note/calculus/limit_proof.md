Consider the function $f(x) = 1 - \frac{1}{2x}$, where $x \ge 2$ and $x \in \mathbb{Z}$. Try to demonstrate
$$
\lim_{n \to +\infty} \prod_{i = 2}^{n}{f(i)} = f(2) \cdot f(3) \cdots = 0
$$
**Proof**  Let the domain of $f(x)$ be $D$, and $g(x) = \ln{f(x)}$. To prove the original proposition, we need to show that
$$
\lim_{n \to +\infty}\sum_{i=2}^{n}{g(i)} = -\infty
$$
Since $0 < f(x) < 1$, $g(x) < 0$ for all $x \in D$. We can also find the first derivative of $g(x)$:
$$
g'(x) = \frac{f'(x)}{f(x)} = \frac{1}{x(2x-1)}
$$
We can see that $g'(x) > 0$ within the domain, so $g(x)$ is strictly increasing. According to the first fundamental theorem of calculus, for all $t \in D$, we have
$$
\left| \int_{t}^{t+1}{g(x) dx} \right| 
< \left| g(t) \right|
$$
Because $g(x) < 0$ constantly holds, we can simplify the above inequality:
$$
g(t)
< \int_{t}^{t+1}{g(x) dx}
$$
By finding the summation of $g(2) + g(3) + \cdots$, we have:
$$
\lim_{n \to +\infty}\sum_{i = 2}^n g(i) < 
\int_{2}^{3}{g(x) dx} + \int_{3}^{4}{g(x) dx} + \cdots = \int_{2}^{+\infty}{g(x) dx}
$$
Now let us find the value of the above integral:
$$
\begin{split}
\int_{2}^{+\infty}{g(x) dx} 
&= \int_{2}^{+\infty}{\ln{(1-\frac{1}{2x})} dx} \\
&= \int_{2}^{+\infty}{\ln{\frac{2x - 1}{2x}} dx} \\
&= \int_{2}^{+\infty}{\ln{(2x-1)} dx} - \int_{2}^{+\infty}{\ln{(2x)} dx} \\
&= \frac{1}{2}\int_{2}^{+\infty}{\ln{(2x-1)} d(2x-1)} - \frac{1}{2}\int_{2}^{+\infty}{\ln{(2x)} d(2x)} \\
&= \frac{1}{2} \left[ (2x-1)\ln{\frac{2x-1}{e}} \right]_2^{+\infty} - \frac{1}{2} \left[ 2x(\ln{\frac{2x}{e}}) \right]_2^{+\infty} \\
&= \frac{1}{2} \left[ \ln{\frac{(2x-1)^{2x-1}}{e^{2x-1}}} - \ln{\frac{(2x)^{2x}}{e^{2x}}} \right]_2^{+\infty} \\
&= \frac{1}{2} \left[ \ln{\frac{e(2x-1)^{2x-1}}{(2x)^{2x}}} \right]_2^{+\infty} \\
&= \frac{1}{2} \left[ \ln{\frac{e(2x-1)^{2x-1}}{(2x)^{2x-1} \cdot (2x)}} \right]_2^{+\infty} \\
&= \frac{1}{2} \left[ 1 - \ln{(2x)} + (2x-1)\ln{\frac{2x-1}{2x}} \right]_2^{+\infty} \\
&= \frac{1}{2}\lim_{x \to +\infty} \left[ 1 - \ln{(2x)} + (2x-1)\ln{\frac{2x-1}{2x}} \right] - (1- \ln{4} + 3 \times \ln{\frac{3}{4}})
\end{split}
$$
Since
$$
\lim_{x \to +\infty}{\ln(2x)} = +\infty \quad \text{and} \quad 
\lim_{x \to +\infty}{\ln{\frac{2x-1}{2x}}} = 0
$$
We obtain
$$
\int_{2}^{+\infty}{g(x) dx} = -\infty \implies \lim_{n \to +\infty}\sum_{i = 2}^n g(i) = -\infty
$$
Therefore, 
$$
\lim_{n \to +\infty} \prod_{i = 2}^{n}{f(i)} = 0
$$
$\square$
