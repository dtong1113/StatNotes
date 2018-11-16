# 4. Probability Rules and Conditional Probability

## Summary

Covers Principles of Inclusion Exclusion, Bayes Law, Law of Total Probability, general math series.


## 4.1 General Methods

Rule 1: $P(S) = 1$

Rule 2: For any event A, $0 \leq P(A) \leq 1$

Rule 3: If $A$ and $B$ are two events with $A \subseteq B$ then $P(A) \leq P(B)$

**Definition**: *De Morgan's Laws* - $\overline{A \cup B} = \overline{A} \cap \overline{B}$ and $\overline{A \cap B} = \overline{A} \cup \overline{B}$

We can use Venn Diagrams to model questions and solve them.

### 4.1.1 Problems

1. $0.07$
2. $0.25$

## 4.2 Rules for Unions of Events

**Definition**: *Addition Law of Probability (Sum Rule)* - $P(A \cup B) = P(A) + P(B) - P(A \cap B)$ . Note that this can be generalized to $n$ events and is also known as the *Principles of Inclusion and Exclusion*. 

**Definition**: *Mutually exclusive* - Events $A$ and $B$ are mutually exclusive if $A \cap B = \empty$ 

We thus get that the probability of the union of $n$ mutually exclusive events is the sum of their individual probabilities. 

$$ P(A_1 \cup A_2 \cup \ldots \cup A_n) = \sum_{i = 1}^{n}P(A_i) $$

### 4.2.1 Problems

1. a) 0.9 b) A and C are mutually exclusive

## 4.3 Intersections of Events and Independence

**Definition**: *Independent events* - two events are independent if and only if $P(A \cap B) = P(A)P(B)$

### 4.3.1 Problems

2. $0.8014$

## 4.4 Conditional Probability

**Definition**: *Conditional probability* - $P(A \vert B) = \frac{P(A \cap B)}{P(B)}$ (provided that $P(B) > 0$)

## 4.5 Product Rules, Law of Total Probability and Bayes' Theorem

**Definition**: *Product Rules* - Let $A, B, C, D, \ldots$ be arbitrary events in a sample space such that they are not mutually exclusive. Then $$P(ABC) = P(A)P(B \vert A) P(C \vert AB)$$ and $P(ABCD) = P(ABC)P(D|ABC)$ and so on.

**Definition**: *Law of Total Probability* - Let $A_1, A_2, \ldots A_k$ be a partition of the sample space $S$ into disjoint (mutually exclusive) events, then if $B$ is an arbitrary event in $S$. We get $$P(B) = \sum_{i = 1}^{k}P(B|A_i)P(A_i) = \sum_{i = 1}^{k}P(BA_i)$$ 

**Definition**: *Bayes' Theorem* - if $A$ and $B$ are events on a sample space $S$, then $$P(A \vert B) = \frac{P(B \vert A)P(A)}{P(B)} = \frac{P(B \vert A)P(A) }{P(B \vert \overline{A})P(\overline{A}) + P(B \vert A)P(A)}$$ 

### 4.5.1 Problems

2. $0.583$

## 4.6 Useful Series and Sums

**Definition**: *Geometric series* - $\sum_{i = 0}^{n- 1}t^i = \frac{1-t^n}{1 - t}$. If $|t| < 1$ then $\sum_{i = 0}^{\infty}t^i = \frac{1}{1 - t}$

**Definition**: *Binomial Theorem* - $(1 + t)^n = \sum_{x = 0}^n {n \choose x}t^x$ for when $n$ is a positive integer and $t$ is real. When $n$ is a decimal we get $(1 + t)^n = \sum_{x = 0}^{\infty} {n \choose x} t^x$. Note that ${n \choose k} = \frac{n(n-1)\ldots(n-k+1)}{k!}$ 

**Definition**: *Multinomial Theorem* - A generalization of the Binomial Theorem is $$(t_1 + t_2 + \ldots + t_k)^n = \sum \frac{n!}{x_1!x_2!\ldots x_k!}t_1^{x_1}t_2^{x_2}\ldots t_k^{x_k}$$ summed over all $x1, x2, \ldots x_k$ such that $\sum_{i = 1}^{ k}  x_i= n$. 

**Definition**: *Hypergeometric Identity* - $$\sum_{x=0}^{\infty}{a \choose x}{b \choose n - x} = {a + b \choose n}$$. The number of ways of picking $n$ numbers from a group of $a + b$ is the same as the sum of picking a specific $x$ from $a$ and $n - x$ from $b$. 

**Definition**: *Exponential Series* - Based on the Maclaurin series expansion on $e^x$. We get $$e^t = \sum_{n = 0}^{\infty}\frac{t^n}{n!}$$ for all real $t$.

### 4.6.1 Problems

1. $$
   \begin{align*}
   	\sum_{x = 0}^n x {n \choose x} p^x (1-p)^{n-x} &= \sum_{x = 0}^n x\frac{n!}{(n-x)!(x!)}p^x(1-p)^{n - x} \\
   	&= \sum_{x = 0}^n \frac{n(n-1)!}{((n-1)-(x-1))!(x-1!)}p^x(1-p)^{n - x} \\
   	&= \sum_{x = 0}^n n{n-1\choose x- 1}p^x(1-p)^{n - x}\\
   	&= np \sum_{x = 0}^n {n-1 \choose x -1}p^{x-1}(1-p)^{n-x} \\
   	&= np (p + (1-p))^{n - 1}
   	&= np
   \end{align*}
   $$




2. Take two derivatives of sum of infinite series.

3. $$
   \begin{align*}
   \sum_{x=0}^\infty{-k \choose x} p^k(p-1)^x &= p^k \sum_{x=0}^\infty{-k \choose x}(p-1)^x \\
   &= p^k (1 + (p - 1))^{-k} \\
   &= 1
   \end{align*}
   $$



## 4.7 Chapter 4 Problems

1. a) 0.75  b) 0.65 c) 0 d) 1 e) 0.35 f) 1

3. $\frac{1}{6}$

5. 0.44

7. f/F = m/M

9. 0.87

14. a) 0.1225 b) 0.245 c) 0.7225