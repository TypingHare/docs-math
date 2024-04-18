rmi# $\int{\sqrt{1+x^2}dx}$

Let $x = \tan{t}$, we have:
$$
\begin{equation}
\begin{split}
\int{ \sqrt{1+x^2}~dx } 
&= \int{ \sqrt{ 1 + \tan^2{t} }~d\tan{t} } \\
&= \int{ \sec{t}~d\tan{t} }
\end{split}
\end{equation}
$$
Let $A = \int{ \sec{t}~d\tan{t} }$. By applying the integration by parts, we have:
$$
\begin{split}
A
&= \sec{t}\tan{t} - \int{ \tan{t}~d\sec{t} } \\
&= \sec{t}\tan{t} - \int{ \tan^2{t}\sec{t}~dt } \\
&= \sec{t}\tan{t} - \int{ (\sec^2{t} - 1)\sec{t}~dt} \\
&= \sec{t}\tan{t} - \int{ \sec{t} \cdot \sec^2{t}~dt + \int{ \sec{t}~dt }} \\
&= \sec{t}\tan{t} - \int{ \sec{t}~d\tan{t} } + \ln{ |\sec{t} + \tan{t}| } + C_0 \\
&= \sec{t}\tan{t} - A + \ln{ |\sec{t} + \tan{t}| } + C_0
\end{split}
$$
Solve the $A$ in the equation, we obtain:
$$
A = \frac{1}{2}( \sec{t}\tan{t} + \ln{ |\sec{t} + \tan{t}| } + C_0)
$$
Plug $t = \arctan{x}$ to $A$, we have:
$$
\begin{split}
A
&= \frac{1}{2}( \sec{\arctan{x}} \tan{\arctan{x}} + \ln{ |\sec{\arctan{x}} + \tan{\arctan{x}}| } + C_0) \\
&= \frac{1}{2}( \sqrt{ 1 + x^2 } \cdot x + \ln{ |\sqrt{ 1 + x^2 } + x| } + C_0) \\
&= \frac{1}{2}x\sqrt{ 1 + x^2 } + \frac{1}{2}\ln{ |x + \sqrt{ 1 + x^2 }| } + C \\
\end{split}
$$
Where $C = \frac{1}{2}C_0$.

