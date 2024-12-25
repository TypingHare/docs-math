# Limit

## 1 Euler's Number

Define $e$ as
$$
e = \lim_{x \rightarrow 0}{(1+x)^{1/x}}
\tag{1.1}
$$
We can find $\lim_{x \rightarrow 0}{(1-x)^{1/x}}$
$$
\lim_{x \rightarrow 0}{(1-x)^{1/x}}
=\lim_{x \rightarrow 0}{\left[ 1+(-x) \right]^{1/x}}
$$
Substitute $t=-x$, we have
$$
\lim_{t \rightarrow 0}{(1+t)^{-1/t}}
=\left[ \lim_{t \rightarrow 0}{(1+t)^{1/t}} \right]^{-1}
=e^{-1}
$$
Therefore,
$$
\lim_{x \rightarrow 0}{(1-x)^{1/x}} = e^{-1}
\tag{1.2}
$$

## 2 Preparation 

### 2.1 Proof of $\lim_{x \rightarrow 0}{\frac{\ln{(1+x)}}{x}}=1$

$$
\begin{equation}
\begin{split}

\lim_{x \rightarrow 0}{\frac{\ln{(1+x)}}{x}}
&=\lim_{x \rightarrow 0}{\ln{(1+x)}^{1/x}} \\
&=\ln{\left[ \lim_{x \rightarrow 0}{(1+x)}^{1/x} \right]} \\
&=\ln{e} \\
&=1

\end{split}
\end{equation}
\tag{2.1}
$$

### 2.2 Proof of $\lim_{x \rightarrow 0}{\frac{a^x-1}{x}} = \ln(a)$

Let $t=a^x-1$, $x=\log_{a}{(1+t)}$, and we have
$$
\begin{equation}
\begin{split}

\lim_{t \rightarrow 0}{\frac{t}{\log_{a}{(1+t)}}}
&= \lim_{t \rightarrow 0}{\frac{\log_{a}{a^t}}{\log_{a}{(1+t)}}} \\
&= \lim_{t \rightarrow 0}{\log_{1+t}{a^t}} \\
&= \lim_{t \rightarrow 0}{t\log_{1+t}{a}} \\
&= \lim_{t \rightarrow 0}{\frac{t\ln{a}}{\ln{(1+t)}}} \\
&= \ln{a} \cdot \lim_{t \rightarrow 0}{\frac{t}{\ln{(1+t)}}} \\
&= \ln{a} \cdot \left[ \lim_{t \rightarrow 0}{\frac{\ln{(1+t)}}{t}} \right]^{-1} \\

\end{split}
\end{equation}
$$
By applying *eq. 2.1*, we can obtain
$$
\lim_{x \rightarrow 0}{\frac{a^x-1}{x}}
= \ln{a}
\tag{2.2}
$$

## 3 Derivatives

### 3.1 Find the derivative of $a^x$

$$
\begin{equation}
\begin{split}

\frac{d}{dx}a^x
&= \lim_{c \rightarrow 0}{\frac{a^{x+c}-a^x}{c}} \\
&= \lim_{c \rightarrow 0}{\frac{a^x(a^{c}-1)}{c}} \\
&= a^x \cdot \lim_{c \rightarrow 0}{\frac{a^{c}-1}{c}} \\

\end{split}
\end{equation}
$$

By applying *eq. 2.2*, we obtain
$$
\frac{d}{dx}a^x
= a^x \cdot \ln{a}
\tag {3.1}
$$

### 3.2 Find the derivative of $\log_{a}{x}$

$$
\begin{equation}
\begin{split}

\frac{d}{dx} log_{a}{x}
&= \lim_{c \rightarrow 0}{\frac{\log_{a}{(x + c)} - \log_{a}{x}}{c}} \\
&= \lim_{c \rightarrow 0}{\frac{\log_{a}{\frac{(x + c)}{x}}}{c}} \\
&= \lim_{c \rightarrow 0}{\frac{\log_{a}{(1+\frac{c}{x})}}{c}} \\

\end{split}
\end{equation}
$$

Let $m=\frac{c}{x}$, $c=mx$, and we have:
$$
\begin{equation}
\begin{split}

\frac{d}{dx} \log_{a}{x}
&= \lim_{m \rightarrow 0}{\frac{\log_{a}{(1+m)}}{mx}} \\
&= \lim_{m \rightarrow 0}{\frac{\frac{\ln{(1+m)}}{\ln{a}}}{mx}} \\
&= \frac{1}{x \ln{a}} \cdot \lim_{m \rightarrow 0}{\frac{\ln{(1+m)}}{m}} \\

\end{split}
\end{equation}
$$
By applying *eq. 2.1*, we obtain
$$
\frac{d}{dx} \log_{a}{x}
= \frac{1}{x \ln{a}}
\tag {3.2}
$$
