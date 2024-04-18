# Monty Hall Problem

**Problem**  Suppose you're on a game show, and you're given the choice of three doors: Behind one door is a car; behind the others, goats. You pick a door, say No. 1, and the host, who knows what's behind the doors, opens another door, say No. 3, which has a goat. He then says to you, "Do you want to pick door No. 2?" Is it to your advantage to switch your choice?

---

**Solution**  Assume that the event $X_i$ is "Behind the door No. $i$ is a car", where $i \in \{ 1, 2, 3\}$. We know that
$$
P(X_i) = \frac{1}{3} \tag{1}
$$
The host knows what's behind the doors, and he opens the door that is not chosen by me and behind which is a goat, and the door is No. 2 as assumed. Assume that event $A$ is "The host opens the door No. 2", we can write the probability that $X_2$ happens, given $A$ happens, which is
$$
P(X_2 \mid A) = \frac{P(X_2 \cap A)}{P(A)} = 0
$$
From this, we can infer that $P(X_2 \cap A) = 0$. Since $P(A) = P(X_1 \cap A) + P(X_2 \cap A) + P(X_3 \cap A)$, we obtain
$$
P(A) = P(X_1 \cap A) + P(X_3 \cap A) \tag{2}
$$
We also know the host never opens door No. 1, as I have taken it. In other words, he can only open door No. 2 and door No. 3. Suppose the car is behind door No. 1, then the probability that the host opens door No. 2 is $\frac12$; otherwise, if the car is behind door No. 3, the host must open door No. 2. Hence,
$$
P(A \mid X_1) = \frac{P(A \cap X_1)}{P(X_1)} = \frac{1}{2}
\quad
P(A \mid X_3) = \frac{P(A \cap X_3)}{P(X_3)} = 1
$$
By plugging equation (1) into the above two equations, we have:
$$
P(A \cap X_1) = \frac{1}{6}
\quad
P(A \cap X_3) = \frac{1}{3}
\tag{3}
$$
With equations (2) and (3), we can find the conditional probability
$$
P(X_1 \mid A) 
= \frac{P(X_1 \cap A)}{P(A)}
= \frac{P(X_1 \cap A)}{P(X_1 \cap A) + P(X_3 \cap A)}
= \frac{1}{3} \\

P(X_3 \mid A) 
= \frac{P(X_3 \cap A)}{P(A)}
= \frac{P(X_3 \cap A)}{P(X_1 \cap A) + P(X_3 \cap A)}
= \frac{2}{3} \\
$$
In conclusion, with the host revealing a goat behind door No. 2, switching my choice offers a $\frac{2}{3}$ probability of winning the prize.