# 3. Probability and Counting Techniques

## Summary

Introduces the addition and multiplication rule. Introduces permutation and combination. Covers how to apply them to count different events. e.g. How many 6 letter passwords contain only 1 vowel?


## 3.1 Addition and Multiplication Rules

**Definition**: *The Addition Rule*: If we can do job $1$ in $p$ ways and job $2$ in  $q$ ways, then we can do job $1$ or job $2$ (but not both) in $p + q$ ways. 

**Definition**: *The Multiplication Rule*: If we can do job $1$ in $p$ ways and for each of these ways, we can do job $2$ in  $q$ ways, then we can do job $1$ and job $2$  in $p \times q$ ways. 

### 3.1.1 Problems

1. a) (i) $S$ is (x, y, z) where $x, y, z \in \{1, 2, 3, 4\}$

   ​    (ii) 4/(4^3)

   ​    (iii) ${4 \choose 3}3!/4^3 = 24/64$

   ​    (iv) $3^3/4^3 = 27/64$

   b) (ii) n/(n^s)

   ​     (iii) ${s \choose n} n!/n^s$ 

   ​     (iv) $(n-1)^s/n^s$ 

2. a) $1/26^2$

   b) 9/1000

3. a) $36^6 + 36^7 + 36^8$

   b) $1000/(36^6 + 36^7 + 36^8)$

## 3.2 Counting Arrangements of Permutations

**Definition**: *Permutation* - when the sample space refers to the set of arrangements or sequences

**Equation**: *Permutation* - $n$ objects can be arranged in $n!$ ways, $k$ objects from a group of $n$ objects can be arranged in $n^{(k)} = n!/(n - k)!$ ways

**Equation**: *Stirling's Approximation* -  $\lim_{n \rightarrow \infty} (n/e)^n \sqrt{2\pi n} = n!$ 

## 3.3 Counting Subsets or Combinations

**Equation**: *Combination* - A subset of size $k$ can be picked from a group of size $n$ in ${n \choose k} = \frac{n^{(k)}}{k!} = \frac{n!}{k!(n-k)!}$ ways. 

**Equation**: *Combination property* - ${n \choose k} = {n -1 \choose k-1} + {n-1 \choose k}$ 

**Equation**: *Binomial Theorem* - $(1 + x)^n = {n \choose 0} + {n\choose1}x + \ldots + {n \choose n} x^n$. 

## 3.4 Number of Arrangements When Symbols Are Repeated

Suppose we need to count the number of arrangements of symbols that are not unique. We can count them by initially treating them as unique objects and then proceeding to remove duplicates. For example, consider the letters in STATISTICS. We have $3$ S's, $2$ T's, $2$ I's, $1$ C and $1$ A for a total of $10$ symbols. There are thus $10!$ ways of arranging them if they were all unique. However, since there are $3$ S's, we divide the final result by $3!$ since it does not matter which $S$ is in which position. This results in $\frac{10!}{3!3!2!1!1!}$. 

We can also come to this conclusion by considering where we place each symbol. We start with $10$ free spots. Then we choose $3$ spots of these $10$ for the S's. Then we choose $2$ of the remaining $7$ for T. We repeat for the remainder of the symbols for a total of ${10 \choose 3}{7 \choose 3} {4 \choose 2}{2 \choose 1}{1 \choose 1} = \frac{10!}{3!3!2!1!1!}$. 

## 3.6 Chapter 3 Problems

1. a) $4/7$

   b) $({5\choose 4} \times 5!)/7! = 5/42$

   c) $({5 \choose 4} {6 \choose 2}{4!})/7! =  5/14$

4. a) (i) $(n-1)^k/n^k$

   ​    (ii) ${n \choose k}k!/n^k$

   b) It is equally likely for each person to get off any floor. This assumption is typically invalid since we expect people to be more likely to get off of key floors (e.g. ground)

7. a) $1/6$

   b) $\frac{10 \choose 3} {10^3}$

10. a) $\frac{7 + 5 + 3 + 1}{9 \choose 3} = \frac{16}{84}$

    b)$ \frac{(2n - 1) + (2n - 3) + \ldots + 1}{2n+1\choose 3}  =  \frac{n^2}{2n+1\choose 3}$

14. a) $5^{(3)}\times 26^3$

    b) (i) $1/26^3$

