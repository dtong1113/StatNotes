# 7. Expected Value and Variance

## Summary

$E(x) = \sum_{x \in A} xf(x)$

$Var(x) = E[(X - \mu)^2] = E(X^2) - \mu^2$ 

$E(Binomial(n, p)) = np$, $Var(Binomial(n, p)) = np(1-p)$

$E(Poisson(\lambda)) = \lambda t = \mu = Var(Poisson(\lambda))$ 

## 7.1 Summarizing Data on Random Variables

A **frequency distribution** gives the number of occurrences for each value of $X$. These can be used to create a frequency histogram.

**Definition**: *sample* - a set of observed outcomes $x1, \ldots, x_n$ for a random variable $X$ is termed a *sample* in probability and statistics

**Definition**: *mean* - the sample mean for a sample is its average

**Definition**: *median* - the median of a sample is a value such that half of the results are below it and half are above it 

**Definition**: *mode* - the mode of a sample is the most frequent occurance

## 7.2 Expectation of a Random Variable

**Definition**: *Expected value* - if $X$ is a discrete random variable with $range(X) = A$ and probability function $f(x)$, the expected value $E(x) = \sum_{x \in A} xf(x)$

Note: $E(x)$ and $\mu$ are identical in meaning 

**Linearity Properties of Expectation**: $E$ is a linear operator. Thus for constants $a$ and $b$, $E(ag(X) + b) = aE(g(x)) + b$ 

## 7.4 Means and Variances of Distributions

The expected value of a Binomial random variable is $np$. 

The expected value of a Poisson random variable is $\lambda t$.

**Definition**: *Variance* - the variance of a random variable $X$, denoted $Var(X)$ or $\sigma ^2$ is $Var(x) = E[(X - \mu)^2]$

We get the two following equations 
$$
\begin{align}
Var(x) = E(X^2) - [E(X)]^2 = E(X^2) - \mu^2 \\
Var(x) = E[X(X - 1)] + E(X) - [E(X)]^2 = E[X(X - 1)] + \mu - \mu^2
\end{align}
$$
This can be derived using the *Linearity Properties of Expectation*.

Also we get that $Var(aX + b) = a^2Var(X)$ for constants $a$ and $b$.

**Definition**: *Standard deviation* - the standard deviation of a random variable $X$ is $\sqrt{Var(X)}$.

The Variance of a Binomial random variable is $np(1 - p)​$.

The Variance of a Poisson random variable is $\mu$.

