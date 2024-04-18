# Discrete Structure I

## 1 Set Theory

### 1.1 Set Notation and Relations

There are three notations to represent a set.

* **Enumeration**: Enclose finite elements with braces, such as $\{ 0,1,2,3\}$​.

* **Standard Symbols**: Positive integers $\mathbb{P}$, natural numbers $\mathbb{N}$, integers $\mathbb{Z}$, and so on.

* **Set-Builder notation**: To define a rational number set:
  $$
  \mathbb{Q} = \{a/b \mid a,b \in \mathbb{Z}, b \neq 0 \}
  $$

A set that has no elements is called an **empty set**, or **null set**. The number of different elements in $A$ is called its **cardinality**, which is denoted as $|A|$. Particularly, $|\emptyset| = 0$.

We say $A$ is a **subset** of $B$ if and only if every element of A is an element of B. We write $A \subseteq B$ to denote that $A$ is a subset of $B$. If $A \subseteq B$ and $B \subseteq A$, then we say $A$ and $B$ are **equal**, which is denoted as $A = B$​. 

If $A \neq \emptyset$, then $A$ is called an **improper subset** of $A$. Other subsets of $A$ are called **proper subsets** of $A$. The empty set is an improper subset of itself.

### 1.2 Basic Set Operation

The **universe set** is the set of all elements under discussion for possible membership in a set. Let $A$ and $B$ be set, and $U$ be the universe set, we have:

* The **intersection** of $A$ and $B$ is defined as $A \cap B = \{x \mid x \in A, x \in B \}$. Two sets are **disjoint** if they have no elements in common, namely, $A \cap B = \emptyset$.
* The **union** of $A$ and $B$ is defined as $A \cup B = \{x \mid x \in A~\text{or}~x \in B \}$. 
* The **complement** of $A$ relative to $B$ is defined as $B-A = \{ x \mid x \in B, x \notin A \}$. Particularly, $A^c = U - A$.
* The **symmetric difference** of $A$ and $B$ is defined as $A \oplus B = (A \cup B) - (A \cap B)$.

### 1.3 Cartesian Products and Power Sets

Let $A$ and $B$ be set, the **cartesian product** of $A$ and $B$ is defined as $A \times B = \{ (a,b) \mid a \in A, b \in B \}$. If both $A$ and $B$ are finite sets, then $|A \times B| = |A| \times |B|$. We can define the cartesian product of three sets similarly. For example:
$$
A \times B \times C = \{ (a,b,c) \mid a \in A, b \in B, c \in C \}
$$
It is common to use  exponents if the sets in a cartesian product are the same: $A^n = A \times A \times ... \times A$, where there are $n$ many $A$ on the right side.

The **power set** of $A$ is the set of all subsets of A, denoted as $\mathcal{P}(A)$. The empty set and all of $A$ are both included in $\mathcal{P}(A)$. The cardinality of a power set is:
$$
|\mathcal{P}(A)| = 2^{|A|}
$$

### 1.4 Binary Representation of Positive Integers

The binary form of $34$ is represented as $10010_{\text{two}}$, where the subscript in the lower right corner indicates the base of the number.

### 1.5 Summation Notation and Generalizations

A summation of a finite set is an expression such as
$$
a_1 + a_2 + \cdots + a_n = \sum_{i=1}^{n}a_i
$$
Where the $i$ is referred to as the **index**, or the index of summation. The expression $a_i$ is the **general term** of the series. The value of $i$​ below the summation symbol is the **initial index**, and the value above the summation symbol is the **terminal index**.

Summation notation can be generalized to many mathematical operations, for example:

* $$
  \bigcap_{i=1}^{n}{A_i} = A_1 \cap A_2 \cdots \cap A_n
  $$

* $$
  \bigcup_{i=1}^{n}{A_i} = A_1 \cup A_2 \cdots \cup A_n
  $$

* $$
  \bigtimes_{i=1}^{n}{A_i} = A_1 \times A_2 \cdots \times A_n
  $$

* $$
  \bigoplus_{i=1}^{n}{A_i} = A_1 \oplus A_2 \cdots \oplus A_n
  $$

## 2 Combinations

### 2.1 Basic Counting Techniques - The Rule of Products

**The rule of products**: If two operations must be performed, and if the first operation can always be performed $p_1$ different ways and the second operation can always be performed $p_2$ different ways, then there are $p_1 \cdot p_2$ different ways that the two operations can be performed.

**Extended rule of products**: If $n$ operations must be performed, and the number of operations for each operation is $p_1, p_2, \cdots, p_n$ respectively, with each $p_i$ independently of previous choices, then the $n$ operations can be performed $p_1 \cdot p_2 \cdots p_n$ different ways.

### 2.2 Permutations

An ordered arrangement of $k$ elements selected from a set of $n$ elements, $0 \le k \le n$, where no two elements of the arrangement are the same, is called a **permutation** of $n$ objects taken $k$ at a time. The total number of such permutations is denoted by $P(n, k)$, which is calculated as:
$$
P(n,k)=\prod_{j=0}^{k-1}(n-j)= \frac{n!}{(n-k)!}
$$
Particularly, $n$ permutations of $n$ is equal to $n!$, namely, $P(n, n) = n!$.

### 2.3 Partitions of Sets and the Law of Addition

A **partition** of a set $A$ is a set of one or more nonempty subsets of $A: A_1, A_2, \cdots$, such that every element of $A$ is in exactly one set, Symbolically,

* $A_1 \cup A_2 \cup \cdots = A$
* If $i \neq j$ then $A_i \cap A_j = \emptyset$.

The subsets in a partition are often referred to as **blocks**. **The basic law of addition**: If $A$ is a finite set, and if $\{ A_1, A_2, \cdots, A_n \}$ is a partition of $A$, then
$$
|A| = \sum_{i=1}^{n}{|A_i|}
$$
**Laws of Inclusion-Exclusion**: Given finite sets $A_1, A_2, A_3$, then

* **The Two Set Inclusion-Exclusion Law**:
  $$
  |A_1 \cup A_2| = |A_1| + |A_2| - |A_1 \cap A_2|
  $$

* **The Three Set Inclusion-Exclusion Law**:
  $$
  |A_1 \cup A_2 \cup A_3| = |A_1| + |A_2| + |A_3| - (|A_1 \cap A_2| + |A_1 \cap A_3| + |A_2 \cap A_2|) + |A \cap A_2 \cap A_3|
  $$

### 2.4 Combinations and the Binomial Theorem

Let $n$ and $k$ be nonnegative integers. The **binomial coefficient** $\binom{n}{k}$ represents the number of combinations of $n$ objects taken $k$ at a time, and is read "$n$ choose $k$". **Binomial Coefficient Formula**: If $n$ and $k$ are nonnegative integers with $0 \le k \le n$, then the number $k$-element subsets of an $n$ element set is equal to
$$
\binom{n}{k} = \frac{n!}{(n-k)! \cdot k!} = \frac{P(n,k)}{k!}
$$
**The Binomial Theorem**: If $n \ge 0$, and $x$ and $y$ are numbers, then
$$
(x+y)^n=\sum_{k=0}^{n}{\binom{n}{k}x^{n-k}y^{k}}
$$

## 3 Logic

### 3.1 Propositions and Logical Operators

A **proposition** is a sentence to which one and only one of the terms *true* or *false* can be meaningfully applied. Let $p$ and $q$ be propositions, **logical operations** are as follows:

* **Logical Negation**: Not p (denoted $\neg p$).
* **Logical Conjunction**: $p$ and $q$ (denoted $p \and q$)​.
* **Logical Disjunction**: $p$ or $q$ (denoted $p \or q$).
* **Conditional Statement**: If $p$ then $q$ (denoted $p \to q$). All of the following are equivalent to "If $p$ then $q$": $p$ implies $q$; $q$ follows from $p$; $p$, only if $q$; $q$, if $p$; $p$ is sufficient for $q$; $q$ is necessary for $p$.
* **Converse**: The converse of the proposition $p \to q$ is $q \to p$​.
* **Contrapositive**: The contrapositive of the proposition $p \to q$ is $\neg q \to \neg p$.
* **Logical Inverse**: The inverse of the proposition $p \to q$ is $\neg p \to \neg q$​.
* **Biconditional Proposition**: $p$ if and only if $q$ (denoted $p \leftrightarrow q$). All of the following are equivalent to "$p$ if and only if $q$": $p$ is necessary and sufficient for $q$; $p$ is equivalent to $q$; If $p$, then $q$, and if $p$, then $p$; If $p$, then $q$​ and conversely.

Apart from the logical negation, all above propositions are **compound propositions**. The truth table for the above logical operations is:

| $p$  | $q$  | $\neg p$ | $p \and q$ | $p \or q$ | $p \to q$ | $q \to p$ | $\neg q \to \neg p$ | $\neg p \to \neg q$ | $p \leftrightarrow q$ |
| ---- | ---- | -------- | ---------- | --------- | --------- | --------- | ------------------- | ------------------- | --------------------- |
| 0    | 0    | 1        | 0          | 0         | 1         | 1         | 1                   | 1                   | 1                     |
| 0    | 1    | 1        | 0          | 1         | 1         | 0         | 1                   | 0                   | 0                     |
| 1    | 0    | 0        | 0          | 1         | 0         | 1         | 0                   | 1                   | 0                     |
| 1    | 1    | 0        | 1          | 1         | 1         | 1         | 1                   | 1                   | 1                     |



### 3.2 Truth Tables and Propositions Generated by a Set

Let $S$ be any set of propositions. A proposition generated by $S$ is any valid combination of propositions in $S$ with conjunction, disjunction, and negation. Or, to be more precise,

* If $p \in S$, then $p$ is a proposition generated by $S$, and
* If $x$ and $y$ are propositions generated by $S$, then so are $(x)$, $\neg x$, $x \or y$, and $x \and y$.

Note that conditional and biconditional can both be generated from conjunction, disjunction, and negation, so they are not included in the definition.

The hierarchy of logical operations:

1. First: Negation
2. Second: Conjunction (*and*)
3. Third: Disjunction (*or*)
4. Fourth: The conditional operation
5. Fifth: The biconditional operation

### 3.3 Equivalence and Implication

An expression involving logical variables that is true in all cases is a **tautology**. An expression involving logical variables that is false for all cases is called a **contradiction**.

Let $S$ be a set of propositions and let $r$ and $s$ be propositions generated by $S$. $r$ and $s$ are **equivalent** if any only if $r \leftrightarrow s$ is a tautology. The equivalence of $r$ and $s$ is denoted $r \Leftrightarrow s$.
$$
p \or \neg p \Leftrightarrow \mathbf{1} \quad p \and \neg p \Leftrightarrow \mathbf{0}
$$
Let $S$ be a set of propositions and let $r$ and $s$ be propositions generated by $S$. We say that $r$ **implies** $s$ if $r \to s$ is a tautology. We write $r \Rightarrow s$ to indicate this **implication**. A commonly used implication called "disjunctive addition" is $p \Rightarrow (p \or q)$.

The **Sheffer Stroke** is defined as:
$$
p \mid q \Leftrightarrow \neg(p \and q)
$$

Note that conditional and biconditional can be represented by $\and$, $\or$, and $\neg$, as:
$$
p \to q = \neg p \or q \quad p \leftrightarrow q = (p \and q) \or (\neg p \and \neg q)
$$

### 3.4 The Laws of Logic

| Name of Law           | Part I                                                       | Part II                                                     |
| --------------------- | ------------------------------------------------------------ | ----------------------------------------------------------- |
| **Commutative Laws**  | $p \or q \Leftrightarrow q \or p$                            | $p \and q \Leftrightarrow q \and p$                         |
| **Associative Laws**  | $(p \or q)\or r \Leftrightarrow p \or (q \or r)$             | $(p \and q) \and r \Leftrightarrow p \and (q \and r)$       |
| **Distributive Laws** | $p \and (q \or r) \Leftrightarrow (p \and q) \or (q \and r)$ | $p \or (q \and r) \Leftrightarrow (p \or q) \and (p \or r)$ |
| **Identity Laws**     | $p \or 0 \Leftrightarrow p$                                  | $p \and 1 \Leftrightarrow p$                                |
| **Negation Laws**     | $p \and \neg p \Leftrightarrow 0$                            | $p \or \neg p \Leftrightarrow 1$                            |
| **Idempotent Laws**   | $p \or p \Leftrightarrow p$                                  | $p \and p \Leftrightarrow p$                                |
| **Null Laws**         | $p \and 0 \Leftrightarrow 0$                                 | $p \or 1 \Leftrightarrow 1$                                 |
| **Absorption Laws**   | $p \and (p \or q) \Leftrightarrow p$                         | $p \or (p \and q) \Leftrightarrow q$                        |
| **DeMorgan's Laws**   | $\neg (p \or q) \Leftrightarrow (\neg p) \and (\neg q)$      | $\neg (p \and q) \Leftrightarrow (\neg p) \or (\neg q)$     |
| **Involution Law**    | $\neg (\neg p) \Leftrightarrow p$                            |                                                             |

### 3.6 Prositions over a Universe

Let $U$ be a nonempty set. A proposition over $U$ is a sentence that contains a variable that can take on any value in $U$​ and that has a definite truth value as a result of any such substitution.

If $p$ is a propositioin over $U$, the **truth set** of $p$ is $T_p = \{ a \in U \mid p(a) \text{ is true} \}$. A proposition is a *tautology* if its truth set is $U$; it is a *contradition* if its truth set is empty. Two propositions, $p$ and $q$, are *equivalent* if $p \Leftrightarrow q$, or $T_p = T_q$​ in terms of truth set.

Truth sets of compound statements:

* $T_{p \and q} = T_p \cap T_q$​
* $T_{p \or q} = T_p \cup T_q$
* $T_{\neg p} = T_p^c$
* $T_{p \leftrightarrow q} = (T_p \cap T_q) \cup (T_p^c \cap T_q^c)$
* $T_{p \rightarrow q} = T_p^c \cap T_q$

### 3.8 Quantifiers

If $p(n)$ is a proposition over $U$ with $T_p \neq \emptyset$, we commonly say "There exists an $n$ in $U$, such that $p(n)$." We abbreviate this with the symbol $(\exists n)_U(p(n))$, or $(\exists n) (p(n))$ if the context if clear. The symbol $\exists$ is called the **existential quantifier**. If $p(n)$ is a proposition over $U$ with $T_p = U$, we commonly say "For all $n$ in $U$, $p(n)$." We abbreviate this with the symbol $(\forall n)_U(p(n))$, or $(\forall n) (p(n))$ if the context if clear. Here, the symbol $\forall$ is called the **universal quantifier**.

When you negate a quantified proposition, the existential and universal quantifiers complement one another:
$$
\neg((\forall n)_U(p(n))) \Leftrightarrow (\exists n)_U(\neg p(n)) \\
\neg((\exists n)_U(p(n))) \Leftrightarrow (\forall n)_U(\neg p(n))
$$
If a proposition has more than one variable, then you can quantify it more than once. It is admissible to *interchange two adjacent identical quantifiers* while preserving the semantic integrity of the sentence. However, the *interchange of two adjacent different quantifiers* is *NOT* permissible, as it may alter the meaning of the sentence.

### 3.7 Mathematical Induction

**The principle of mathematical induction**: Let $p(n)$ be a proposition over the positive integers. If

1. $p(1)$​ is true, and
2. for all $n \ge 1$, $p(n) \Rightarrow p(n+1)$,

then $p(n)$ is a tautology. This can be simplified as
$$
p(1) \and (\forall n \ge 1. p(n) \Rightarrow p(n+1)) \Rightarrow p(n)
$$
The truth of $p(1)$ is called the **basis** for the induction proof. The premise that $p(n)$ is true in the second part is called the **induction hypothesis**. The proof that $p(n)$ implies $p(n+1)$​ is called the **induction step** of the proof.

**The generalized principle of mathematical induction**: If $p(n)$ is a proposition over $\{ k_0, k_0 + 1, k_0 + 2, \cdots \}$, where $k_0$ is any integer, then $p(n)$ is a tautology if

1. $p(k_0)$ is true, and
2. for all $n \ge 0$, $p(n) \Rightarrow p(n+1)$​.

>**Example**  Prove that for all $n \ge 1$, $n^3+2n$ is a multiple of $3$.
>
>**Proof**  
>
>*Base case*: When $n = 1$, $1^3 + 2 \times 1 = 1 + 2 = 3$. Since $3$ is clearly a multiple of $3$, the base case holds.
>
>*Inductive step*: Assume that statement holds for some arbitrary positive integer $k$. That is, assume $k^3 + 2k$ is a multiple of $3$. Now, we need to prove that the statement holds for $k+1$. That is, we need to show that $(k+1)^3 + 2(k+1)$ is a multiple of $3$.
>$$
>\begin{split}
>(k+1)^3+2(k+1)
>=& k^3 + 3k^2 + 3k + 1 + 2k + 2
>=& k^3 + 2k + 3(k^2 + k + 1)
>\end{split}
>$$
>We know that $k^3 + 2k$ is a multiple of $3$ by the induction hypothesis. Additionally, $3(k^2+k+1)$ is also a multiple of 3 since it is clearly a product of $3$. Therefore, $(k+1)^3+2(k+1)$ is the sum of two multiple of $3$, hence it is also a multiple of $3$.

### 3.9 A Review of Methods of Proof

All theorems in mathematics can be expressed in form "If P then C" ($P \Rightarrow C$), where $P$ is the **premise** (or **hypothesis**), and $C$ is the **conclusion**; or in the form of $P \Leftrightarrow C$, which is equivalent to $P \Rightarrow C$ and $C \Rightarrow P$. There are two basic methods for proving $P \Rightarrow C$:

* **Directly**: Assume $P$ is true and prove $C$ is true.
* **Indirectly** (or **by contradiction**): Assume $P$ is true and $C$​ is false, and prove that this leads to a contradiction of some premises, theorems, or basic truth.

> **Example**  Prove that $\sqrt{2}$ is irrational.
>
> Assume that $\sqrt{2}$ is rational. This means it can be expressed as a fraction in its simplest form, where $\sqrt{2} = \frac{a}{b}$, where $a$ and $b$ are integers with no common factors other than $1$. This implies that:
> $$
> \frac{a^2}{b^2} = 2 \quad \implies \quad a^2 = 2b^2
> $$
> Now, $a^2$ is an even number, and $a$ must also be even because the number of an odd number is odd. Let $a = 2k$ where $k$ is another integer. Substituting $a = 2k$ into the equation $a^2 = 2b^2$, we have:
> $$
> b^2 = 2a^2
> $$
> Likewise, $b$ is also an even number. Now, both $a$ and $b$ are even, then they have a common factor of $2$, which contradicts our assumption that $a$ and $b$ have no common factors other than $1$.

## 4 More on Sets

### 4.1 Methods of Proof for Sets

A **counterexample** is an exmaple that disproves a statement. Let $A$ be a subset of a universal set $U$ and let $u \in U$. To use this method we note that exactly one of the following is true: $u \in A$ or $u \not\in A$. Denote the situation where $u \in A$ by 1 and that where $u \not\in A$ by 0. The **set-membership** table for $A \cup B$ is:

| $A$  | $B$  | $A \cup B$ |
| ---- | ---- | ---------- |
| 0    | 0    | 0          |
| 0    | 1    | 1          |
| 1    | 0    | 1          |
| 1    | 1    | 1          |

This table illustrates that $u \in A \cup B$ if and only if $u \in A$ or $u \in B$​.

*Proof techniques*:

1. State or restate the theorem so you understand what is given (the hypothesis) and what you are trying to prove (the conclusion).
2. (1) To prove that $A \sube B$, we must show that if $x \in A$, then $x \in B$. (2) To prove that $A = B$, we must show (a) $A \sube B$ and (b) $B \sube A$.

### 4.2 Laws of Set Theory

The laws of set theory can be derived using the laws of logic [the laws of logic](# 3.4 The Laws of Logic).

### 4.3 Minsets

Let $\{ B_1, B_2, \cdots, B_n \}$ be a set of subsets of a set $A$. Sets of the form $D_1 \cap D_2 \cap \cdots \cap D_n$, where each $D_i$ may be either $B_i$ or $B_i^c$, is called a minset generated by $B_1, B_2, \cdots, B_n$. Note that an ***empty set is not a minset***. Let $A$ be a set and let $B_1, B_2, \cdots, B_n$ be subset of $A$. The set of nonempty minsets generated by $B_1, B_2, \cdots, B_n$ is a partition of $A$. 

A set is said to be in **minset normal form** when it is expected as the union of zero or more distinct nonempty minsets. Notes:

* The union of zero sets is the empty set, $\emptyset$.
* Minset normal form is also called **canonical form**.

### 4.4 The duality Principle

Let $S$ be any identity involving sets and the operations complement, intersection, and union. If $S*$ is obtained from $S$ by making the substitutions $\cup \to \cap$, $\cap \to \cup$, $\emptyset \to U$, and $U \to \emptyset$, then the statement $S*$ is also true and it is called the **dual** of the statement $S$.

> **Example**  The dual of $(A \cap B) \cup (A \cap B^c) = A$ is $(A \cup B) \cap (A \cup B^c) = A$.

## 6 Relations

### 6.1 Relations Between Two Sets

Let $A$ and $B$ be sets. A **relation** from $A$ into $B$ is any subset of $A \times B$. Particularly, A relation from a set $A$ into itself is called a relation on $A$. 

Let $A$, $B$, and $C$ be sets, and relations $r \sube A \times B$, $s \sube B \times C$. The **composition** of $r$ and $s$, written $rs$, is the set of pairs of the form $(a, c) \in A \times C$, where $(a,c) \in rs$ if and only if there exists $b \in B$ such that $(a, b) \in r$ and $(b, c) \in s$.

### 6.3 Properties of Relations

Let $A$ be a set and let $r$ be a relation on $A$. Then $r$ is **reflexive** if and only if $ara$ for all $a \in A$; $r$ is **symmetric** if and only if whenever $arb$ then $bra$ is true; $r$ is **antisymmetric** if and only if whenever $arb$ and $a \neq b$ then $bra$ is false; $r$ is **transitive** if and only if whenever $arb$ and $brc$ then $arc$​.

A relation on a set $A$ that is *reflexive*, *antisymmetric*, and *transitive* is called a **partial ordering** on $A$. A set on which there is a partial ordering relation defined is called a **partially ordered set** or **poset**.

A relation on a set $A$ is called an **equivalence** relation if and only if it is reflexive, symmetric, and transitive. Let $r$ be an equivalence relation on $A$, and $a \in A$. The **equivalence class** of $a$ is a set, $[a]$, of all elements to which $a$ is related.
$$
[a] = \{b \in A : arb\}
$$
 The set of all equivalence classes with respect to $r$ is denoted $A/r$, read "$A$ mod $r$". Let $r$ be an equivalence relation on $A$, then the set of all distinct equivalence classes determined by $r$ form a partition of $A$.

Let $n$ be a positive integer, $n \ge 2$. We define **congruence modulo** n to be the relation $\equiv_n$ defined on the integers by
$$
a \equiv_n b \Leftrightarrow n \mid (a-b)
$$

## 7 Functions

### 7.1 Definition and Notation

A function from a set $A$ into a set $B$ is a relation from $A$ into $B$ such that each element of $A$ is related to exactly one element of the set $B$. The set $A$ is called the **domain** of the function and the set $B$ is called the **codomain**. Note that:

* Each element in $A$, the domain of $f$, must be related to some element of $B$, the codomain.
* If $(a, b) \in f$ and $(a, c) \in f$, then $b = c$.

Given two sets $A$ and $B$, the set of all functions from $A$ into $B$ is denoted $B^A$. Note that $|B^A| = |B|^{|A|}$

Let $f: A \to B$, read "Let $f$ be a function from the set $A$ into the set $B$." If $a \in A$, then $f(a)$ is called the image of $a$ under $f$. We write $f(a) = b$ to indicate that the image of $a$ is $b$.

The range of a function is the set of images of its domain. If $f: X \to Y$, then the range of $f$ is denoted $f(X)$, and
$$
f(X) = \{f(a) \mid a \in X\} = \{ b \in Y \mid \exists a \in X~\text{such that}~f(a)=b\}
$$
Note that $f(X) \sube Y$. $f(X)$ is also read as "the image of the set $X$ under the function $f$" or simply "the image of $f$​".

If the domain of a function is the Cartesian product of two sets, for example, $G: \mathbb{N} \times \mathbb{N} \to \mathbb{N}$ defined by $G((n_1, n_2)) = n_1+n_2$, then we drop one set of parentheses and write $G(1,2)=3$ instead of $G((1,2)) = 3$.

### 7.2 The Properties of Functions

A function $f: A \to B$ is **injective** if
$$
\forall a, b \in A, a \neq b \Rightarrow f(a) \neq f(b)
$$
An injective function is called an **injection**, or a **one-to-one function**.

A function $f: A \to B$ is **surjective** if $f(A) = B$. A surjective function is called a **surjection**, or an **onto function**.

A function $f: A \to B$​ is **bijective** if it is both injective and surjective. Bijective functions are also called one-to-one, onto functions.

Two sets are said to have the same cardinality if there exists a bijection between them. If a set has the same cardinality as the set $\{ 1,2,3, \cdots, n\}$, then we say its cardinality is $n$. If a set is finite or has the same cardinality as the set of positive integers, it is called a **countable set**.

**The Pigeonhole Principle**   Let $X$ and $Y$ be finite sets, and $f: X \to Y$. If $n \ge 1$ and $|X| \gt n|Y|$, then there exists an element of $Y$ that is the image under $f$ of at least $n+1$ elements of $X$​.

### s7.3 Function Composition

Let $f, g: A \to B$, then $f = g$ if and only if $f(x) = g(x)$ for all $x \in A$. Let $f: A \to B$ and $g: B \to C$. Then the **composition** of $f$ followed by $g$, written $g \circ f$ is a function from $A$ into $C$ defined by $(g \circ f)(x) = g(f(x))$, which is read "$g$ of $f$ of $x$". Function composition is associative: If $f: A \to B$, $g: B \to C$, and $h: C \to D$, then $h \circ (g \circ f) = (h \circ g) \circ f$​.

Let $f: A \to A$, $f^1 = f$, and for $n \ge 1$, $f^{n+1} = f \circ f^n$. That is, $f^{n+1}(a) = f(f^n(a))$ for all $a \in A$.

The composition of injections is an injection. The composition of surjections is a surjection. For a set $A$, the **identify function** on $A$ is a function from $A$ onto $A$, denoted by $i$ or $i_A$, such that $i(a) = a$ for all $a \in A$. Note that $f \circ i = i \circ f$.

Let $f: A \to A$. If there exists a function $g: A \to A$ such that $g \circ f = f \circ g = i$, then $g$ is called the **inversion** of $f$ and is denoted $f^{-1}$. $f^{-1}$ exists if and only if $f$ is a bijection. A bijection of a set $A$ into itself is called a permutation of $A$.

## 8 Recursion and Recurrence Relations
