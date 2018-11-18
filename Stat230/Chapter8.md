# 8. Continuous Random Variables

## Summary

Introduction to continuous random variables and their probability density functions.
$$
E[g(x)] = \int_{-\infty}^{\infty} g(x)f(x)dx
$$

- Continuous Uniform Distribution
- Exponential Distribution
- Normal Distribution

## 8.1 General Terminology and Notation

**Definition**: *Continuous random variable* - a random variable where the range is an interval on the real number line

Note that for a continuous random variable, the probability of any specific point on the number line is zero. However, we can assign a probability for a interval of values.

**Definition**: *Cumulative distribution function* - $F(x) = P(X \leq x)$

The same properties of a cdf apply.

1. $F(x)$ is defined for all real $x$.
2. $F(x)$ is a non-decreasing function of $x$ for all real $x$
3. $lim_{x \rightarrow - \infty} F(x) = 0$ and $lim_{x \rightarrow \infty} F(x) = 1$
4. $P(a < X \leq b) = F(b) - F(a)$

**Definition**: *Probability density function* - the p.d.f for a continuous random variable $X$ is the derivative $f(x) = \frac{dF(x)}{dx}$ where $F(x)$ is the c.d.f for $X$. The p.d.f represents the relative likelihood of different outcomes.

The following are properties of a probability density function:

1. $P(a \leq X \leq b) = F(b) - F(a) = \int_a^b f(x)dx$ 
2. $f(x) \geq 0$
3. $\int_{-\infty}^{\infty} f(x)dx = \int_{allx} f(x)dx = 1$ 
4. $F(x) = \int_{-\infty}^x f(u)du$

Although for any specific point, P(x) = 0, we have finite precision so we accept values within a certain $\Delta$. We get $P(x - 0.5 \Delta \leq X \leq x + 0.5 \Delta) \approx f(x)\Delta$ 

**Definition**: *Quantiles and Percentiles* - suppose $X$ is a continuous random variable with c.d.f $F(x)$. The $p$th quantile of $X$ is the value $q(p)$, such that $P[X \leq q(p)] = p$. The value $q(p)$ is also the $100pth$ percentile of the distribution. $q(0.5)$ is the median of $X$.

We can find the pdf and cdf for a random variable $Y$ which is a function of $X$ by following these steps:

1. Write the cumulative distribution function of $Y$ as a function of $X$.
2. Use $F_X(x)$ to find $F_Y(y)$. To find pdf, differentiate the expression for $F_Y(y)$.
3. Find the range of values of $y$. 

For a continuous random variable we define 
$$
E[g(x)] = \int_{-\infty}^{\infty} g(x)f(x)dx
$$
We can apply the same formula for Variance as with discrete random variables. $Var(x) = E[(X - \mu)^2]$.

## 8.2 Continuous Uniform Distribution

**Definition**: *Continuous Uniform distribution* - If $X$ takes values in some interval $[a, b]$ with all sub-intervals of a fixed length being equally likely, then $X$ has a continuous uniform distribution. $X \sim U(a,b)$

The mean of $U(a, b)$ is $(a + b)/2$ and $Var(x) = (b - a)^2/12$ 

We can compute random variables with respect to other distributions by using $U(0, 1)$. We can do this by solving for when the $F(x) = U(0, 1)$.

## 8.3 Exponential Distribution

**Definition**: *Exponential distribution* - a continuous random variable $X$ is said to have an Exponential distribution if its probability density function is of the form $f(x) = \lambda e^{- \lambda x}$ when $x > 0$, otherwise, $f(x) = 0$

Consider a Poisson process for events. Let $X$ be the length of time we wait for the first event occurrence. We get that $X$ has an Exponential distribution.

We get that the cdf of the Exponential distribution is $F(x) = 1 - e^{-\lambda x}$ 

To solve for the mean and variance of the Exponential distribution involves integration by parts. Instead we can use the gamma functions.

**Definition**: *Gamma function* - extension of factorials beyond the integers to the positive real numbers. $\Gamma(\alpha) = \int_0^{\infty}y^{\alpha - 1}e^{-y} dy$

The Gamma function has the following properties:

1.  $\Gamma(\alpha) = (\alpha - 1)\Gamma(\alpha - 1)$ for $\alpha > 1$
2. $\Gamma(\alpha) = (\alpha - 1)!$
3. $\Gamma(\frac{1}{2}) = \sqrt{\pi}​$

Note that if $\lambda$ is the average rate of occurrence in a Poisson process, then the average waiting time is the parameter $\theta$.

We get that the mean of the Exponential distribution is $\mu = \theta$ and $\sigma^2 = Var(X) = \theta^2$

## 8.5 Normal Distribution

**Definition**: *Normal distribution* - a random variable $X$ has a Normal distribution if it has a probability density function of the form $f(x) = \frac{1}{\sqrt{2 \pi}\sigma}e^{-\frac{1}{2}(\frac{x - \mu}{\sigma})^2}$ where $\mu \in \mathbb{R}$ and $\sigma > 0$. We write $X \sim N(\mu, \sigma^2)$

For a normal distribution, $E(x) = \mu$ and $Var(X) = \sigma^2$, which is why its p.d.f is written in terms of $\mu$ and $\sigma^2$.

The c.d.f of the Normal distribution $N(\mu,\sigma^2)$ is $F(x) = \int_{-\infty}^x \frac{1}{\sqrt{2\pi}\sigma}e^{-\frac{1}{2}(\frac{y - \mu}{\sigma})^2} dy$ for $x \in \mathbb{R}$.

The **standard** Normal distribution is $Z \sim N(0, 1)$. We can use the $Z$ table to calculate the probability of certain values of a normal distribution. 

Consider $X \sim N(\mu, \sigma^2)$ and $Z \sim N(0, 1)$.
$$
P(X \leq x) = P(Z \leq \frac{x - \mu}{\sigma})
$$
This can be proven by manipulating the c.d.f of $N(\mu, \sigma^2)$. 