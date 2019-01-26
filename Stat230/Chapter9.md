# 9. Multivariate Distributions

## Summary

We define probability functions, independence, conditional probability in terms of Multi-variate distributions (similar to events)

## 9.1 Basic Terminology and Techniques

**Definition**: *Joint probability function* - consider two discrete random variables $X$ and $Y$, the joint probability function is $f(x, y) = P(X = x, Y = y)$. 

In general we get:
$$
f(x_1, x_2, \ldots, x_n) = P(X_1 = x_1, _2 = x_2, \ldots, X_n = x_n)
$$
and
$$
\sum_{all(x, y)} f(x, y) = 1
$$
**Definition**: *Marginal probability function* - distribution of $X$ obtained by summing values from the joint probability function. Allows us to eliminate variables that are not of interest

**Definition**: *Independent random variables* - random variables $X$ and $Y$ are independent if $f(x, y) = f_1(x)f_2(y)$ for all values $(x, y)$. 

**Definition**: *Conditional probability function* - $f_1(x|y) = \frac{f(x, y)}{f_2(y)}$ provided  $f_2(y) > 0$

**Theorem**: (*29*) If $X \sim Poisson(\mu_1)$ and $Y \sim Poisson(\mu_2)$ independently then $T = X + Y \sim Poisson(\mu_1 + \mu_2)$. `

**Theorem**: (*30*) If $X \sim Binomial(n, p)$ and $Y \sim Binomial(m, p)$ independently then $T = X + Y \sim Binomial(n+m, p)$. 

## 9.2 Multinomial Distribution

 **Definition**: *Multinomial distribution* - suppose an experiment is repeated independently $n$ times with $k$ distinct types of outcome each time. Let the probabilities of these $k$ types be $p_1, p_2, \ldots, p_k$ each time. Let $X_i$ represent the number of times the $i$'th result occurs. Then $(X_1, X_2, \ldots, X_k)$ has a Multinomial distribution. $f(x_1, x_2, \ldots, x_k) = \frac{n!}{x_1!x_2!\ldots x_k!}p_1^{x_1}p_2^{x_2}\ldots p_k^{x_k}$ 

## 9.3 Markov Chains

**Definition**: *Markov chain* - consider a sequence of (discrete) random variables $X_1, X_2, \ldots$ which take integer values $1, 2, \ldots, N$ called states. We assume that for a certain matrix $P$ (transition probability matrix), the conditional probabilities are given by corresponding elements of the matrix; that is, $P(X_{n+1} = j |X_n = i, X_{n-1} = i_1, \ldots) = P(X_{n+1} = j | X_n = i)$. In other words, the probability of the next state is determined by only the current state.

We can consider the state of $X_n$ to be a distribution. Suppose that the chain randomly chooses a state for $X_0$. Then the distribution of $X_1$ is given by $P(X_1 = j) = \sum_{i = 1}^N P_{ij}q_i$ where $P_{ij}$ represents the probability for state $i$ to transition to state $j$ and $\vec{q}$ is the column vector of the distribution of values at a certain time.

**Definition**: *Limiting distribution of a Markov Chain* - the limiting distribution of a Markov chain is a vector ($\vec{\pi}$) of long run probabilities of the individual states such that $\pi_i = \lim_{t \rightarrow \infty} P[X_t = i]$.

Suppose convergence to this distribution holds for an initial distribution $\vec{q}$, we get $\vec{q}^T P^n \rightarrow \vec{\pi}^T$ as $n \rightarrow \infty$. Then notice that $\vec{q}^T P^{n+1} \rightarrow \vec{\pi}^T$ as $n \rightarrow \infty$. So $\vec{\pi}^T$ must have the property that $\vec{\pi}^TP = \vec{\pi}^T$. 

**Definition**: *Stationary distribution of a Markov chain* - is the column vector $\vec{\pi}$ of probabilities of the individual states such that $\vec{\pi}P = \vec{\pi}$ 

If a Markov Chain has transition probability matrix with all rows identical, it corresponds to independent random variables. The current state (or previous state) has no effect in determining the next state.

Note that a Markov Chain can only have multiple stationary distribution if and only if $\mathrm{rank}(P - I) = 0$ or $P = I$.

## 9.4 Expectation for Multivariate Distributions: Covariance and Correlation

We can extend our definition of expected value to multiple discrete random variables. $E[g(X, Y)] = \sum_{all(x, y)} g(x, y)f(x,y)$. 

Additionally, multivariate expectation also follows properties of linearity.

**Definition**: *Covariance* - measures the strength of the relationship between two random variables. $Cov(X,Y)$ or $\sigma_{XY} = E[(X - \mu_X)(Y - \mu_Y)]$. We also get $Cov(X, Y) = E(XY) - E(X)E(Y)$. 

Not that if $X, Y$ are independent then $E(XY) = E(X)E(Y)$ so thus $Cov(X, Y) = 0$. Note however, that this is not reversible. If $Cov(X,Y) = 0$ then it does not necessarily mean that $X$, $Y$ are independent variables.

The equation can also be rearranged to get $E(XY) = E(X)E(Y) + Cov(X, Y)$. 

**Theorem**: $(36)$ Suppose random variables $X$ and $Y$ are independent random variables. Then, if $g_1(X)$ and $g_2(Y)$ are any two functions $E[g_1(X)g_2(Y)] = E[g_1(X)]E[g_2(Y)]$ 

Note that since $Cov(X,Y)$ is dependent on the values $X$ and $Y$ take, the actual numerical value of $Cov(X,Y)$ has no interpretation. Instead we consider the correlation coefficient.

**Definition**: *Correlation coefficient* - is a measure of the strength of the linear relationship between $X$ and $Y$. $\rho = \frac{Cov(X,Y)}{\sigma_X \sigma_Y}$. This is the covariance scaled to lie in the interval $[-1, 1]$ where $1$ implies linear correlation and $-1$ implies inverse linear correlation.

## 9.5 Mean and Variance of a Linear Combination of Random Variables

**Results for Means**:

1. $E(aX + bY) = aE(X) + bE(Y) = a \mu_X + b \mu_Y$ when $a$ and $B$ are constants.
2. $E(\sum_{i = 1}^n X_i) = \sum_{i = 1}^{n}E(X_i)$ 
3. Let $X_1, X_2, \ldots, X_n$ be random variables with mean $\mu$. Suppose the sample mean is $\overline{X} = \frac{1}{n} \sum_{i = }^n X_i$, then $E(\overline{X}) = \mu$. 

**Results for Covariance**:

1. $Cov(X, X) = E[(X - \mu_X)(X - \mu_X)] = E[(X - \mu)^2] = Var(X)$
2. $Cov(aX + bY, cU + dV) =acCov(X, U) + adCov(X, V) + bcCov(Y, U) + bdCov(Y, V)$ where a, b, c and d are constants.

**Results for Variance**:

1. Variance of linear combinations: $Var(aX + bY) = a^2Var(X) + b^2Var(Y) + 2abCov(X,Y)$

2. Variance of a sum of independent random variables: Let $X$ and $Y$ be independent. Since $Cov(X, Y) = 0$ then $Var(X + Y) = \sigma_X^2 + \sigma_Y^2$

3. Variance of a general linear combination of random variables: Let $a_i$ be constants and $Var(X_i) = \sigma_i^2$. Then $Var(\sum_{i = 1}^n a_iX_i) = \sum_{i = 1}^n a_i^2\sigma_i^2 + 2\sum_{i = 1}^n \sum_{j = i + 1}^n a_i a_j Cov(X_i, X_j)$ 

4. Variance of a linear combination of independent random variables: 

   a) If $X_1, X_2, \ldots, X_n$ are independent then  $Var(\sum_{i = 1}^n a_iX_i) = \sum_{i = 1}^n a_i^2 \sigma_i^2​$  

   b) If $X_1, X_2, \ldots, X_n$ are independent and all have the same variance $\sigma^2$, then $Var(\overline{X}) = \frac{\sigma^2}{n}$

## 9.6 Linear Combinations of Independent Normal Random Variables

