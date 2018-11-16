# 5. Discrete Random Variables

## Summary

## 5.1 Random Variables and Probability Functions

**Definition**: *Random variable* - a numerical-valued variable that represents outcomes in an experiment or random process (e.g. X = # of heads when flipping a coin 3 times has a range of [0, 3])

Each outcome of a random variable represents an event. (X = 1, then {HTT, THT, TTH}).

**Definition**: *Discrete random variables* - take integer values or, more generally, values in a countable set (elements can be placed in a one-one correspondence with a subset of the positive integers)

**Definition**: *Continuous random variables* - take values in some interval of real numbers like $(0, 1)​$ or $(0, \infty)​$ or $(-\infty, \infty)​$ 

**Definition**: *Probability function* - for a discrete random variable $X$ with $range(X) = A$, the probability function $f(x) = P(X = x)$ defined for all $x \in A$

**Definition**: *Probability distribution* - the probability distribution of a r.v. $X$ with range $A$ is the set of pairs $\{(x, f(x)) : x \in A\}$

All probability functions have the two properties:

1. $f(x) \geq 0$ for all $x \in A$
2. $\sum_{\forall x \in A} f(x) = 1$

**Definition**: *Cumulative distribution function* - the cdf of $X$ is the function usually denoted by $F(x) = P(X \leq x)$ 

All cumulative distribution functions have the following properties:

1. $F(x)$ is a non-decreasing function of $x$ for all $x \in \mathbb{R}$ 
2. $0 \leq F(x) \leq 1$ for all $x \in \mathbb{R}$
3. $\lim_{x \rightarrow -\infty} F(x) = 0$ and $lim_{x \rightarrow \infty} F(x) = 1$

## 5.2 Discrete Uniform Distribution

**Definition**: *Discrete uniform distribution* - Suppose $X$ takes values $a, a+1, a+2, \ldots, b$ with all values being equally likely. Then $X$ has a discrete Uniform distribution on the set $\{a, a+1, \ldots, b\}$. $P(X = x) = \frac{1}{(b - a + 1)}$ and $P(X \leq x) = \frac{x - a + 1}{b - a + 1}$ for $x \in [a, b]$. 

## 5.3 Hypergeometric Distribution

**Definition**: *Hypergeometric distribution* - Suppose we have $N$ objects with two types (success, failure) and we want to pick $n$ objects at random without replacement. Let us suppose there are $r$ successes. If $X$ is number of successes obtained then $X$ has a Hypergeometric distribution. $f(x) = P(X = x) =  \frac{{r \choose x}{N-r \choose n -x}}{N \choose n}$

## 5.4 Binomial Distribution

**Definition**: *Binomial distribution* - suppose an experiment has two distinct outcomes (success, failure) with probability of success $p$. Let $X$ be the number of successes obtained, then $X$ has a Binomial distribution. We write $X \sim B(n, p)$. $f(x) = P(X = x) = {n \choose x}p^x(1- p)^{n - x}$

## 5.5 Negative Binomial Distribution

**Definition**: *Negative binomial distribution* - suppose we are running an experiment with two distinct outcomes that is repeated with the same probability of success. If $X$ be the number of failures obtained before the $k$'th success then $X$ has a Negative Binomial distribution. We write $X \sim NB(k, p)$. $f(x) = P(X = x) = {x + k - 1 \choose x}p^k(1-p)^x$. 

## 5.6 Geometric Distribution

**Definition**: *Geometric distribution* - consider the *Negative Binomial* distribution with $k = 1$. We get that $X \sim Geometric(p)$. $f(x) = P(X = x) = (1 - p)^xp$. 

**Definition**: *Bernoulli Trials* - experiments which are independent, have 2 distinct outcomes (S and F), have the same probability of success

## 5.7 Poisson Distribution from Binomial

**Definition**: *Poisson distribution* - consider a Binomial distribution as $n \rightarrow \infty$ and $p \rightarrow 0$ where $np = \mu$ remains constant. We get $X \sim Poisson(\mu)$. We get $f(x) = \frac{\mu^x e^{-\mu}}{x!}$ for $x = 0, 1, 2 \ldots​$

## 5.8 Poisson Distribution from Poisson Process

**Definition**: *Poisson process* - Consider a situation in which an event occurs at random points in time or space. If it follows the conditions: *Independence*, *Individuality*, *Homogenity/Uniformity*

1. **Independence**: the number of occurrences in non-overlapping intervals are independent
2. **Individuality**: for sufficiently short time periods of lengths, the probability of 2 or more events occurring in the interval is close to zero
3. **Homogenity/Uniformity**: events occur at a uniform or homogenous rate $\lambda$ over time so the probability of one occurence in an interval $(t, t + \Delta t)$ is approximately $\lambda \Delta t$ 

We get that $\lambda$ is referred to as the **intensity** or **rate of occurrence** parameter. It is the average rate of occurence of events per unit of time. Then $\lambda t = \mu$ is the average number of occurences in $t$ units of time.

We can consider the following questions when thinking about whether or not a distribution is Poisson:

1. Can we specify in advance the maximum value which X can take?
2. Does it make sense to ask how often the event did not occur?

If either of the above are valid then the distribution is NOT Poisson.