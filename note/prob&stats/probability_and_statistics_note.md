
# Probability and Statistics

## 1 Probability

In the study of statistics, we are concerned basically with the presentation and interpretation of **chance outcomes**, which refers to the results or events that occur randomly or unpredictably. The statistician is often dealing with either **numerical data**, representing counts or measurements, or **categorical data**, which can be classified according to some criterion. We refer to any recording of information as an **observation** and any process that generates a set of data as an **experiment**.

> In the statistical experiment of tossing a coin, there are two possible outcomes, heads and tails. Another experiment might be the launching of a missile and observing its velocity at specified times. 

**Definition 1.1**  The set of all possible outcomes of a statistical experiment is called the **sample space** and is represented by the symbol $S$.

Each outcome in a sample space is called an **element**, a **member**, or a **sample point** of the sample space. In some experiments, it is helpful to list the elements of the sample space systematically using a [**tree diagram**](https://thirdspacelearning.com/gcse-maths/probability/probability-tree-diagram/). Sample spaces with a large or infinite number of sample points are best described by a **statement** or **rule method** (the set-builder notation in set theory).
$$
S = \{ (x,y) \mid x^2 + y^2 \le 4 \}
$$
**Definition 1.2**  An **event** is a subset of a sample space.

**Definition 1.3**  The **complement** of an event $A$ with respect to $S$ is the subset of all elements of $S$ that are not in $A$. We denote the complement of $A$ by the symbol $A'$.

**Definition 1.4**  The **intersection** of two events $A$ and $B$, denoted by the symbol $A \cap B$, is the event containing all elements that are common to $A$ and $B$.

**Definition 1.5**  Two events $A$ and $B$ are **mutually exclusive**, or **disjoint**, if $A \cap B = \emptyset$, that is, if $A$ and $B$ have no elements in common.

**Definition 1.6**  The **union** of sets $A$ and $B$, denoted as $A \cup B$, comprises all elements that are members of either set $A$, set $B$, or both sets simultaneously.

**Rule 1.1 (multiplication rule)**  If an operation can be performed in $n_1$ ways, and if for each of these ways, a second operation can be performed in $n_2$ ways, then the two operations can be performed together in $n_1n_2$​ ways.

**Rule 1.2 (generalized multiplication rule)**  If an operation can be performed in $n_1$ ways, and if for each of these operations, a second operation can be performed in $n_2$ ways, and for each of the first two a third operation can be performed in $n_3$ ways, and so forth, then the sequence of $k$ operations can be performed in $n_1n_2 \cdots n_k$​ ways.

**Definition 1.7**  A **permutation** is an arrangement of all or part of a set of objects.

**Theorem 1.1**  The number of permutations of $n$ objects is $n!$.

**Proof**  For $n = 1$, there is only one object, so the number of permutations is $1! = 1$. Assume that the number of permutations of $k$ objects is $k!$, where $k$ is a positive integer. We need to show that the number of permutations of $(k+1)$ objects is $(k+1)!$. 

Consider a set of $(k+1)$ objects. We can choose one of these objects to be in the first position, which leaves $k$ objects for the remaining positions. By the inductive hypothesis, the number of permutations of these $k$ objects is $k!$. Since there are $(k+1)$ choices for the first position, the total number of permutations of these $(k+1)$ objects is $(k+1) \cdot k! = (k+1)!$​, according to **Rule 1.1**.

Therefore, by mathematical induction, the number of permutations of $n$ objects is $n!$ for all positive integers $n$​. $\square$

**Theorem 1.2**  The number of permutations of $n$ distinct objects taken $r$ at a time is
$$
_nP_r=\frac{n!}{n-r!}
$$
**Proof**  We have $n$ distinct objects. To select $r$ objects from $n$, we have $n$ choices for the first object, $(n-1)$ choices for the second object, until $(n-r+1)$ choices for the $r$-th object. Thus, by **Rule 1.2**, the number of ways to select and arrange $r$ objects from $n$ distinct objects is given by:
$$
_nP_r=n \times (n-1) \times \cdots (n-r+1) = \frac{n!}{n-r!}
$$
$\square$

Permutations that occur by arranging objects in a circle are called **circular permutations**. Two circular permutations are not considered different unless corresponding objects in the two arrangements are preceded or followed by a different object as we proceed in a clockwise direction.

**Theorem 1.3**  The number of permutations of $n$ objects arranged in a circle is $(n-1)!$​.

**Proof**  For $n = 1$, there is only one object, so the number of circular permutations is $(1-1)! = 1$. Assume that the number of circular permutations of $k$ objects is $(k-1)!$. We need to show that the number of permutations of $(k+1)$ objects is $k!$.

Consider inserting an object into a circle consisting of $k$ objects. There are $k$ different slots to insert the new object. By the inductive hypothesis and **Rule 1.1**, the total number of permutations of these $(k+1)$ objects is $k \cdot (k-1)! = k!$​.

Therefore, by the mathematical induction, The number of circular permutations of $n$ objects is $(n-1)!$. $\square$

**Theorem 1.4**  The number of distinct permutations of $n$ things of which $n_1$ are of one kind, $n_2$ of a second kind, $\cdots$, $n_k$ of a $k$-th kind is:
$$
\frac{n!}{n_1!n_2! \cdots n_k!}
$$
**Theorem 1.5**  The number of ways of partitioning a set of $n$ objects into $r$ cells with $n_1$ elements in the first cell, $n_2$ elements in the second, and so forth, is
$$
\binom{n}{n_1,n_2,\cdots,n_r} = \frac{n!}{n_1!n_2! \cdots n_r!}
$$

> *In how many ways can 7 graduate students be assigned to 1 triple and 2 double hotel rooms during a conference?*
>
> **Solution**  The total number of possible partitions would be
> $$
> \binom{7}{3,2,2} = \frac{7!}{3! \times 2! \times 2!} = 210
> $$

**Theorem 1.6**  The number of combinations of $n$ distinct objects taken $r$ at a time is:
$$
\binom{n}{r} = \binom{n}{r, n-r} = \frac{n!}{r!(n-r)!}
$$
**Proof**  Consider partitioning $n$ distinct objects into 2 cells, $r$ objects and $(n-r)$ objects. From **Theorem 1.5** we can obtain the result immediately. $\square$

> *How many different letter arrangements can be made from the letters in the word STATISTICS?*
>
> **Solution**  We have 10 total letters, with 2 letters ($S$ and $T$) appearing 3 times each, letter $I$ appearing twice, and letters $A$ and $C$ appearing once each. By applying **Theorem 1.6**, we obtain
> $$
> \binom{10}{3, 3, 2, 1, 1} = \frac{10!}{3! \times 3! \times 2! \times 1! \times 1!} = 50400
> $$

**Definition 1.9**  The **probability** of an event $A$ is the sum of the weights of all sample points in $A$​, Therefore,
$$
0 \le P(A) \le 1,\quad P(\emptyset) = 0,\quad \text{and}\quad P(S) = 1
$$
Furthermore, if $A_1, A_2, \cdots$ is a sequence of mutually exclusive events, then
$$
P(A_1 \cup A_2 \cup \cdots) = P(A_1) + P(A_2) + \cdots
$$
**Rule 1.3**  If an experiment can result in any one of $N$ different equally likely outcomes, and if exactly $n$ of these outcomes correspond to an event $A$, then the probability of the event $A$ is
$$
P(A) = \frac{n}{N}
$$
There are two different approaches to understanding and interpreting probability. According to the **relative frequency** definition of probability, the probability of an event is determined by observing the relative frequency with which the event occurs in a large number of trials or experiments. The **subjective definition** of probability is based on personal judgments, beliefs, or assessments about the likelihood of an event occurring.

**Theorem 1.7**  If $A$ and $B$​ are two events, then
$$
P(A \cup B) = P(A) + P(B) - P(A \cap B)
$$
**Proof**  The $P(A \cup B)$ is the sum of the probabilities of the sample points in $A \cup B$, and $P(A) + P(B)$ is the sum of all the possibilities in $A$ plus the sum of all the probabilities in $B$. Therefore, we have added the probabilities in $(A \cap B)$ twice. Since these probabilities add up to $P(A \cup B)$, we must subtract these probabilities once to obtain the sum of the probabilities in $A \cup B$. $\square$

**Corollary 1.1**  If $A$ and $B$ are mutually exclusive (See **Definition 1.5**), then
$$
P(A \cup B) = P(A) + P(B)
$$
**Proof**  If $A$ and $B$ are mutually exclusive, then $P(A \cap B) = 0$. Therefore, this corollary is an immediate result of **Theorem 1.7**.  $\square$

**Corollary 1.2**  If $A_1, A_2, \cdots, A_n$ are mutually exclusive, then
$$
P(A_1 \cup A_2 \cup \cdots \cup A_n) = P(A_1) + P(A_2) + \cdots + P(A_n)
$$
A collection of events $\{ A_1, A_2, \cdots, A_n \}$ of a sample space $S$ is called a **partition** of $S$ if the events are mutually exclusive and $A_1 \cup A_2 \cup \cdots \cup A_n = S$.

**Corollary 1.3**  If $A_1, A_2, \cdots, A_n$ is a partition of sample space $S$, then
$$
P(A_1 \cup A_2 \cup \cdots \cup A_n) = P(S) = 1
$$
**Theorem 2.8**  For three events $A$, $B$, and $C$,
$$
P(A \cup B \cup C) = P(A) + P(B) + P(C) - P(A \cap B) - P(A \cap C) - P(B \cap C) + P(A \cap B \cap C)
$$
**Theorem 2.9**  If $A$ and $A'$ are complementary events, then
$$
P(A) + P(A') = 1
$$
**Proof**  According to **Definition 1.3**, we know that $A \cap A' = \emptyset$, and $A \cup A' = S$. By applying Theorem 1.7, we have
$$
P(S) = P(A \cup A') = P(A) + P(A') - P(A \cap A') = P(A) + P(A') - P(\emptyset)
$$
From **Definition 1.9**, we can substitute $P(S)$ with $1$, and $P(\emptyset)$ with $0$, therefore
$$
P(A) + P(A') = 1
$$
$\square$

The probability of an event $B$ occurring when it is known that some event $A$ has occurred is called a **conditional probability** and is denoted by $P(B \mid A)$, which is usually read as "the probability that $B$ occurs given that $A$ occurs" or simply "the probability of $B$, given $A$."

**Definition 1.10**  The conditional probability of $B$, given $A$, denoted by $P(B \mid A)$, is defined by
$$
P(B \mid A) = \frac{P(A \cap B)}{P(A)},\quad \text{provided}~P(A) > 0
$$

>The probability that a regularly scheduled flight departs on time is $P(D) = 0.83$; the probability that it arrives on time is $P(A) = 0.82$; and the probability that it departs and arrives on time is $P(D \cap A) = 0.78$. Find the probability that a plane (a) arrives on time, given that it departs on time, (b) departed on time, given that it has arrived on time, and (c) arrives on time, given that it did not depart on time.
>
>**Solution**  (a) The probability that a plane arrives on time, given that it departed on time is
>$$
>P(A \mid D) = \frac{P(A \cap D)}{P(D)} = \frac{0.78}{0.83} = 0.94
>$$
>(b) The probability that a plane departed on time, given that it has arrived on time is
>$$
>P(D \mid A) = \frac{P(D \cap A)}{P(A)} = \frac{0.78}{0.82} = 0.95
>$$
>(c) The probability that a plane did not depart on time is $P(D') = 1 - P(D) = 1 - 0.83 = 0.17$. The probability that a place did not depart on time, but arrives on time is $P(A \cap D') = P(A) - P(D \cap A)$. Hence, the probability that a plane arrives on time, given that it did not depart on time is
>$$
>P(A \mid D') = \frac{P(A \cap D')}{P(D')} = \frac{P(A) - P(D \cap A)}{P(D')} = \frac{0.82 - 0.78}{0.17} = 0.24
>$$

**Definition 1.11**  Two events $A$ and $B$ are **independent** if and only if
$$
P(B \mid A) = P(B) \quad \text{or} \quad P(A \mid B) = P(A)
$$
assuming the existence of conditional probabilities. Otherwise, $A$ and $B$ are **dependent**.

**Theorem 1.10**  If in an experiment the events $A$ and $B$ can both occur, then
$$
P(A \cap B) = P(A)P(B \mid A),\quad \text{provided}~P(A)>0
$$
**Theorem 1.11 (product rule/multiplicative rule)**  Two events $A$ and $B$ are **independent** if and only if
$$
P(A \cap B) = P(A)P(B)
$$
**Proof**  We need to show that

1. If $A$ and $B$ are independent, then $P(A \cap B) = P(A)P(B)$:

   According to **Definition 1.10** and **Definition 1.11**
   $$
   P(B) = P(B \mid A) = \frac{P(A \cap B)}{P(A)}
   $$
   Therefore,
   $$
   P(A \cap B) = P(A)P(B)
   $$

2. If $P(A \cap B) = P(A)P(B)$, then $A$ and $B$​ are independent:

   By **Definition 1.10**, we know that
   $$
   P(A \cap B) = P(A) P(B) = \frac{P(A \cap B)}{P(B \mid A)} P(B)
   $$
   Therefore,
   $$
   P(B) = P(B \mid A)
   $$
   Hence, **from Definition 1.11,** we can conclude that $A$ and $B$ are independent.  $\square$

**Theorem 1.12 (generalized product rule)**  If, in an experiment, the events $A_1, A_2, \cdots, A_k$ can occur, then
$$
P(A_1 \cap A_2 \cap \cdots \cap A_k) = P(A_1)P(A_2 \mid A_1)P(A_3 \mid A_1 \cap A_2) \cdots P(A_k \mid A_1 \cap A_2 \cap \cdots \cap A_{k-1})
$$
If the events $A_1, A_2, \cdots, A_k$ are independent, then
$$
P(A_1 \cap A_2 \cap \cdots \cap A_k) = P(A_1)P(A_2) \cdots P(A_k)
$$
**Definition 1.12**  A collection of events $A = \{ A_1, A_2, \cdots, A_n \}$ are mutually independent if for any subset of $A$, $A_{i1}, \cdots, A_{ik}$, for $k \le n$, we have
$$
P(A_{i1} \cap \cdots \cap A_{ik}) = P(A_i) \cdots P(A_{ik})
$$
**Theorem 1.13 (theorem of total probability/rule of elimination)**  If the events $B_1, B_2, \cdots, B_k$ constitute a partition of the sample space $S$ such that $P(B_i) \ne 0$ for $i = 1,2, \cdots, k$, then for any event $A$ of $S$,
$$
P(A) = \sum_{i=1}^{k}P(B_i \cap A) = \sum_{i=1}^{k}P(B_i)P(A \mid B_i)
$$
**Proof**  The event $A$ is seen to be the union of the mutually exclusive events
$$
B_1 \cap A, B_2 \cap A, \cdots, B_k \cap A
$$
that is,
$$
A = (B_1 \cap A) \cup (B_2 \cap A) \cup \cdots \cup (B_k \cap A)
$$
Using **Corollary 1.2** and **Theorem 1.10**, we have
$$
P(A) 
= P(B_1 \cap A) + P(B_2 \cap A) \cdots P(B_k \cap A) 
= \sum_{i=1}^{k}{P(B_i \cap A)} 
= \sum_{i=1}^{k}{P(B_i)P(A \mid B_i)}
$$
$\square$

**Theorem 1.14 (Bayes' Rule)**  If the events $B_1, B_2, \cdots, B_k$ constitute a partition of the sample space $S$ such that $P(B_i) \ne 0$ for $i = 1, 2, \cdots, k$, then for any event $A$ in $S$ such that $P(A) \ne 0$ and $r = 1,2, \cdots k$, 
$$
P(B_r \mid A) 
= \frac{P(B_r \cap A)}{\sum_{i=1}^{k}P(B_i \cap A)}
= \frac{P(B_r)P(A \mid B_r)}{\sum_{i=1}^{k}{P(B_i)P(A \mid B_i)}}
$$
**Proof**  By the definition of conditional probability,
$$
P(B_r \mid A) = \frac{P(B_r \cap A)}{P(A)}
$$
We also know that $P(B_r \cap A) = P(A \cap B_r) = P(B_r)P(A \mid B_r)$. Using **Theorem 2.13** in the denominator, we have
$$
P(B_r \mid A) 
= \frac{P(B_r)P(A \mid B_r)}{\sum_{i=1}^{k}{P(B_i)P(A \mid B_i)}}
$$
$\square$

## 2 Random Variables and Probability Distributions

**Definition 2.1**  A **random variable** is a function that associates a real number with each element in the sample space.

The random variable for which $0$ and $1$​ are chosen to describe the two possible values is called a **Bernoulli random variable**.

**Definition 2.2**  If a sample space contains a finite number of possibilities or an unending sequence with as many elements as there are whole numbers, it is called **discrete sample space**.

**Definition 2.3**  If a sample space contains an infinite number of possibilities equal to the number of points on a line segment, it is called a **continuous sample space**.

A random variable is called a **discrete random variable** if its set of possible outcomes is countable. When a random variable can take on values on a continuous scale, it is called a **continuous random variable**.

**Definition 2.4**  The set of ordered pairs $(x, f(x))$ is a **probability function**, **probability mass function**, or **probability distribution** of the discrete random varaible $X$ if, for each possible outcome $x$,

1. $f(x) \ge 0$,
2. $\sum_{x}{f(x)} = 1$​, and
3. $P(X = x) = f(x)$.

>A shipment of 20 similar laptop computers to a retail outlet contains $3$ that are defective. If a school makes a random purchase of $2$ of these computers, find the probability distribution for the number of defectives.
>
>**Solution**  Let $X$ be a random variable whose values $x$ are the possible numbers of defective computers purchased by the school. Then $x$ can only take the numbers $0$, $1$, and $2$. Now,
>$$
>f(0) = P(X = 0) = \frac{\binom{3}{0}\binom{17}{2}}{\binom{20}{2}} = \frac{68}{95}
>$$
>
>$$
>f(1) = P(X = 1) = \frac{\binom{3}{1}\binom{17}{1}}{\binom{20}{2}} = \frac{51}{190}
>$$
>
>$$
>f(0) = P(X = 0) = \frac{\binom{3}{2}\binom{17}{0}}{\binom{20}{2}} = \frac{3}{190}
>$$

**Definition 2.5**  The **cumulative distribution function** $F(x)$ of a discrete random variable $X$ with probability distribution $f(x)$ is
$$
F(x) = P(X \le x) = \sum_{t \le x}{f(t)},\quad \text{for}~x \in \mathbb{Z}
$$
**Definition 2.6**  The function $f(x)$ is a **probability density function** for the continuous random variable $X$, defined over the set of real numbers, if

1. $f(x) \ge 0$, for all $x \in R$,
2. $\int_{-\infty}^{+\infty}{f(x)dx} = 1$, and
3. $P(a \lt X \lt b) = \int_{a}^{b}{f(x)dx}$.

**Definition 2.7**  The **cumulative distribution function** $F(x)$ of a continuous random variable $X$ with density function $f(x)$ is
$$
F(x) = P(X \le x) = \int_{-\infty}^{x}{f(t)dt},\quad \text{for}~x \in \mathbb{R}
$$

>For the density function
>$$
>\begin{cases} 
>  \frac{x^2}{3}, & -1 < x < 2 \\
>  0, & \text{elsewhere}.
>\end{cases}
>$$
>Evaluate $P(0 \lt X \le 1)$.
>
>**Solution**  For $-1 \lt x \lt 2$, the cumulative distribution function
>$$
>F(x) = \int_{-\infty}^{x}{\frac{t^2}{3} dt}
>= \left. \frac{t^3}{9} \right|_{-1}^x
>= \frac{1 + x^3}{9}
>$$
>Therefore,
>$$
>F(x) =
>\begin{cases}
>	0, & x \lt -1, \\
>	\frac{1 + x^3}{9}, & -1 \le x \lt 2, \\
>	1, & x \ge 2.
>\end{cases}
>$$
>Now,
>$$
>P(0 \lt x \le 1) = F(1) - F(0) = \frac{2}{9} - \frac{1}{9} = \frac{1}{9}
>$$

**Definition 2.8**  The function $f(x,y)$ is a **joint probability distribution** or **probability mass function** of the discrete random variables $X$ and $Y$​ if

1. $f(x,y) \ge 0$ for all $(x, y)$,
2. $\sum_{x}\sum_{y}f(x,y) = 1$, and
3. $P(X = x, Y = y) = f(x, y)$.

For any region $A$ in the $xy$ plane, $P \left[ (X,Y) \in A \right] = \sum\sum_{A}f(x,y)$​.

**Definition 2.9**  The function $f(x, y)$ is a **joint density function** of the continuous random variables $X$ and $Y$ if

1. $f(x,y) \ge 0$ for all $(x, y)$,
2. $\int_{-\infty}^{+\infty}\int_{-\infty}^{+\infty}{f(x,y)dxdy} = 1$, and
3. $P \left[ (X,Y) \in A \right] = \int\int_A{f(x,y)dxdy}$, for any region $A$ in the $xy$ plane.

**Definition 2.10**  The **marginal distribution** of $X$ alone and of $Y$​ alone are
$$
g(x) = \sum_y{f(x, y)}\quad \text{and} \quad h(y) = \sum_x{f(x, y)}
$$
for the discrete case, and
$$
g(x) = \int_{-\infty}^{+\infty}{f(x,y)}dy \quad \text{and} \quad h(y)=\int_{-\infty}^{+\infty}f(x,y)dx
$$
for the continuous case.

The term marginal is used here because, in the discrete case, the values of $g(x)$ and $h(y)$ are just the marginal totals of the respective columns and rows when the values of $f(x,y)$​ are displayed on a rectangular table.

**Definition 2.11**  Let $X$ and $Y$ be two random variables, discrete or continuous. The conditional distribution of the random variable $Y$ given that $X = x$ is
$$
f(y \mid x) = \frac{f(x,y)}{g(x)},\quad \text{provided}~g(x) \gt 0
$$
Similarly, the conditional distribution of $X$ given that $Y = y$ is
$$
f(x \mid y) = \frac{f(x,y)}{h(y)},\quad \text{provided}~h(y) \gt 0
$$
**Definition 2.12**  Let $X$ and $Y$ be two random variables, discrete or continuous, with the joint probability distribution $f(x,y)$ and marginal distributions $g(x)$ and $h(y)$, respectively. The random variables $X$ and $Y$ are said to be **statistically independent**, if and only if
$$
f(x,y)=g(x)h(y)
$$
for all $(x,y)$​ within their range.

Definition 3.13  Let $X_1, X_2, \cdots, X_n$ be $n$ random variables, discrete or continuous, with the joint probability distribution $f(x_1, x_2, \cdots, x_n)$ and marginal distribution $f_1(x_1), f_2(x_2), \cdots, f_n(x_n)$, respectively. The random variables $X_1, X_2, \cdots, X_n$ are said to be **mutually statistically independent** if and only if
$$
f(x_1, x_2, \cdots, x_n) = f_1(x_1)f_1(x_n) \cdots f_n(x_n)
$$
for all $(x_1, x_2, \cdots, x_n)$ within their range.

## 3 Mathematical Exception

**Definition 3.1**  Let $X$ be a random variable with probability distribution $f(x)$. The **mean**, or **expected value**, of $X$ is
$$
\mu = E(X) = \sum_{x}{xf(x)}
$$
if $X$ is discrete, and
$$
\mu = E(X) = \int_{-\infty}^{+\infty}{xf(x)dx}
$$
if $X$ is continuous.

>A lot containing $7$ components is sampled by a quality inspector; the lot contains $4$ good components and $3$ defective components. A sample of $3$ is taken by the inspector. Find the expected value of the number of good components in this sample.
>
>**Solution**: Let $X$ represent the number of good components in the sample. The probability distribution of $X$ is
>$$
>f(x)=\frac{\binom{4}{x}\binom{3}{3-x}}{\binom{7}{3}},\quad x=0,1,2,3
>$$
>Simple calculations yield $f(0)=1/35$, $f(1)=12/35$, $f(2)=18/35$, and $f(3)=4/35$. Therefore,
>$$
>\mu = E(X) = (0)(\frac{1}{35}) + (1)(\frac{12}{35})+ (2)(\frac{18}{35})+ (3)(\frac{4}{35}) = 1.7
>$$
>Thus, if a sample of size $3$, is selected at random over and over again from a lot of $4$ good components and $3$ defective components, it will contain, on average, $1.7$ good components.

**Theorem 4.1**  Let $X$ be a random variable with probability distribution $f(x)$. The expected value of the random variable $g(X)$ is
$$
\mu_{g(X)} = E \left[ g(X) \right] = \sum_{x}{g(x)f(x)}
$$
if $X$ is discrete, and
$$
\mu_{g(X)} = E \left[ g(X) \right] = \int_{-\infty}^{+\infty}{g(x)f(x)dx}
$$
if $X$​ is continuous.

> Let $X$ be a random variable with density function
> $$
> f(x)=
> \begin{cases}
> \frac{x^2}{3}, & -1 \lt x \lt 2, \\
> 0, & \text{elsewhere}.
> \end{cases}
> $$
> Find the expected value of $g(X) = 4X + 3$.
>
> **Solution**  By **Theorem 4.1**, we have
> $$
> E(4X+3)
> = \int_{-1}^{2}{\frac{x^2}{3}(4x+3)dx}
> = \frac{1}{3}\int_{-1}^{2}{(4x^3 + 3x^2)dx}
> = \frac{1}{3} \left[ (x^4 + x^3) \right]_{-1}^{2}
> = 8
> $$

**Definition 4.2**  Let $X$ and $Y$ be random variables with joint probability distribution $f(x,y)$. The mean, or expected value, of the random variable $g(X, Y)$ is
$$
\mu_{g(X,Y)} = E \left[ g(X,Y) \right] = \sum_{x}\sum_{y}{g(x,y)f(x,y)}
$$
if $X$ and $Y$ are discrete, and
$$
\mu_{g(X,Y)} = E \left[ g(X,Y) \right] 
= \int_{-\infty}^{+\infty}\int_{-\infty}^{+\infty}{g(x,y)f(x,y)dxdy}
$$
if $X$​ are $Y$​ are continuous.

**Definition 4.3**  Let $X$ be a random variable with probability distribution $f(x)$ and mean $\mu$. The **variance** of $X$ is
$$
\sigma^2 = E[(X-\mu)^2]=\sum_{x}{(x-\mu)^2f(x)}
$$
if $X$ is discrete, and
$$
\sigma^2 = E[(X-\mu)^2] = \int_{-\infty}^{+\infty}{(x - \mu)^2f(x)dx}
$$
If $X$ is continuous. The positive square root of the variance, $\sigma$ is called the **standard deviation** of $X$​.

**Theorem 4.2**  The variance of a random variable $X$ is
$$
\sigma^2 = E(X^2) - \mu^2
$$

## 4 Some Discrete Probability Distributions

