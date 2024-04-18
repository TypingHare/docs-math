If $y'+p(x)y=Q(x)$, Try to prove the following formula:
$$
y=\frac{1}{I(x)} \left[ \int{I(x)Q(x)dx + C} \right]
$$
Where $I(x)=e^{\int{p(x)dx}}$.
***
**Proof**  Let
$$
I(x)=e^{\int{p(x)dx}}
$$
By applying natural logarithm, we have:
$$
\ln{I(x)}=P(x)
$$
Then find the derivative with respect to $x$ on both side, we obtain:
$$
\frac{I'(x)}{I(x)}=P(x)
$$
Multiply both sides of the original equation by $I(x)dx$:
$$
I(x)dy+I(x)P(x)ydx=I(x)Q(x)dx
$$
Replace $I(x)P(x)$ with $I'(x)$:
$$
I(x)dy+I'(x)ydx=I(x)Q(x)dx \tag{1}
$$
Find the differential of $I(x)y$:
$$
d \left[ I(x)y \right]= I'(x)ydx + I(x)dy \tag{2}
$$
We can find that the left hand side of the equation (1) is the same as the right hand side of the equation (2), so we have:
$$
d \left[ I(x)y \right]=I(x)Q(x)dx
$$
Integrate both sides:
$$
I(x)y + C_0 = \int{I(x)Q(x)dx}
$$
Move $C_0$ to the right hand side, and divide both sides by $I(x)$:
$$
y=\frac{1}{I(x)}\left[  \int{I(x)Q(x)dx} + C \right]
$$
Where $C=-C_0$.