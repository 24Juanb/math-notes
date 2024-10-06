---
layout: post
title: "Week 1: Methods of Proof"
date: 2024-10-05
categories: math notes
---


## Chapter 1: Methods of Proof

#### 1.1: Proof by Contradiction


1. Prove $\sqrt{2} + \sqrt{3} + \sqrt{5}$ is irrational.  

Assume $\sqrt{2} + \sqrt{3} + \sqrt{5} = r$ for some rational $r$. $\sqrt{2} + \sqrt{3} = r - \sqrt{5}$, and squaring both sides gives that $2\sqrt{6} + 2r \sqrt{5}$ must be rational. Squaring this itself yields something like $a + b\sqrt{30} + c$ for rational $a, b, c$, and since this expression must be rational, $\sqrt{30}$ must be rational.  
Write $\sqrt{30} = \frac{p}{q}$ for coprime integers $p, q$. So, $30(q^2) = (p^2)$, but 30 is not a perfect square, implying $\gcd(p, q) \neq 1$, so $p, q$ cannot be coprime, contradicting our initial assumption that $r$ is rational.

2. Show that no set of nine consecutive integers can be partitioned into two sets with the product of the elements of the first set equal to the product of the elements of the second set. 

Since 9 is odd, one set must have 4 integers while the other must have 5 integers. These integers are strictly increasing, so let’s set the two products as $a(a+1)(a+2)(a+3)(a+4) = (a+5)(a+6)(a+7)(a+8)$. The right-hand side is a quartic expression, so it grows at a slower rate than the left-hand side. Plugging in $a = 6$ gives $LHS > RHS$. Hence, $a \leq 5$. For $a = 3, 4, 5$, only one $a+k$ will be divisible by 11, a prime number. Therefore, there is no solution. Similarly, for $a = 1, 2$, the set has at most one element divisible by 7, another prime, ruling out solutions for these values as well.

3. Find the least positive integer $n$ such that any set of $n$ pairwise relatively prime integers greater than 1 and less than 2005 contains at least one prime number.  

To have pairwise relatively prime integers, each integer must be divisible by a distinct prime number. So, we can have $k$ pairwise relatively prime integers as long as there are $k$ primes less than $n$. However, none of these integers are allowed to be prime themselves, so each must be of the form $p_1^2, p_2^2, \dots, p_k^2$. Since there are 14 primes less than $\sqrt{2005}$, any set with $n \geq 15$ must contain at least one prime.

4. Every point of three-dimensional space is colored red, green, or blue. Prove that one of the colors attains all distances.  

Assume there exist distances $r, g, b$ such that none of the distances are attained by points of the respective colors. Without loss of generality, assume $r \geq g \geq b$. Choose a red point $R$ and draw a circle of radius $r$ centered at $R$. Since $g$ and $b$ are less than $r$, not all points on this circle can be green or blue, or they would contradict the assumptions on distance. Thus, there must be points of both colors on the circle, leading to a contradiction when analyzing the distances between points.

5. The union of nine planar surfaces, each of area equal to 1, has a total area of 5. Prove that the overlap of some two of these surfaces has an area greater than or equal to $\frac{1}{9}$.  

Assume for contradiction that the overlap of any two surfaces is less than $\frac{1}{9}$. Then, the total area of the union of the surfaces would be greater than 5, as we add areas beyond the allowable total. Since this is impossible, there must be at least one overlap greater than or equal to $\frac{1}{9}$.

6. Show that there does not exist a function $f : \mathbb{Z} \to {1, 2, 3}$ such that $f(x) \neq f(y)$ for all $x, y \in \mathbb{Z}$ where $|x - y| \in {2, 3, 5}$.  

Assume such a function exists. Let $f(k) = a$. Then $f(k+2) = b$ and $f(k+5) = c$, where $a, b, c$ are distinct. But $f(k+3) = b$, meaning $f(k+2) = f(k+3)$, a contradiction.

7. Show that there does not exist a strictly increasing function $f : \mathbb{N} \to \mathbb{N}$ satisfying $f(2) = 3$ and $f(mn) = f(m)f(n)$ for all $m, n \in \mathbb{N}$.  

Assume such a function exists and let $f(3) = k$. Since $2^3 < 3^2$, we know $f(2^3) < f(3^2)$, implying $k^2 > 27$. Hence


8. Determine all functions $f : \mathbb{N} \to \mathbb{N}$ satisfying  
$$xf(y) + yf(x) = (x + y)f(x^2 + y^2)$$ 
for all positive integers $x$ and $y$.  

Assume for contradiction that there is some non-constant function $f$ satisfying the given equation. Then, there exist integers $a, b$ such that $f(b) > f(a)$. Now,  
$(a + b)f(a) < af(b) + bf(a) < (a + b)f(b)$, implying  
$(a + b)f(a) < (a + b)f(a^2 + b^2) < (a + b)f(b)$, meaning  
$f(a) < f(a^2 + b^2) < f(b)$.  
This leads to an infinite squeeze between $f(a)$ and $f(b)$, which is a contradiction since $f$ only takes natural number values. Hence, the only solution is a constant function, $f = k$, for some constant $k \in \mathbb{N}$.

9.  Show that the interval $[0, 1]$ cannot be partitioned into two disjoint sets $A$ and $B$ such that $B = A + a$ for some real number $a$.  

Assume for contradiction that such a partition exists. Without loss of generality, let $A = [0, x]$ and $B = (x, 1]$. Notice that $0 + a = x$ and $x + a = 1$, so $a = x = \frac{1}{2}$. However, this leads to a contradiction because $A$ and $B$ are disjoint, meaning $B \neq A + \frac{1}{2}$ since $0 + \frac{1}{2}$ is in $A$.

10. Let $n > 1$ be an arbitrary real number, and let $k$ be the number of positive prime numbers less than or equal to $n$. Select $k + 1$ positive integers such that none of them divides the product of all the others. Prove that there exists a number among the chosen $k + 1$ that is bigger than $n$.  
Call these primes $p_1, p_2, \dots, p_k$ with $p_k \leq n$. Assume for contradiction that we have $k+1$ positive integers with none of them dividing the product of the others. This can only work if these integers are coprime. However, the smallest set of coprime numbers we can form are prime numbers, meaning the $(k+1)$'st prime number must be greater than or equal to $n$.
#### 1.2: Mathematical Induction

>[!question] Fermat's little theorem: Prove that $n^p-n \equiv 0 (\mod p)$ for any prime $p$ and positive integer $n$
>base case ($n == 1$): $1-1 \equiv 0 (\mod p)$
>assume $k^p-k \equiv 0 (\mod p)$
>then, $$(k+1)^p - (k+1) = k^p + 1 + \sum_i^{p-1} \binom{p}{i} k^i - (k+1)$$ and since $\sum_i^{p-1} \binom{p}{i} \equiv 0 (\mod p)$ and $k^p - p \equiv 0 (\mod p)$, the induction is complete as $$(k+1)^p - (k+1) \equiv 0(\mod p)$$

RETURN TO EXAMPLE 3 WHEN I HAVE MORE ENERGY

11. Prove for all positive integers $n$ the identity 
$$
\frac{1}{n+1} + \frac{1}{n+2} + \cdots + \frac{1}{2n} = 1 - \frac{1}{2} + \frac{1}{3} - \cdots + \frac{1}{2n-1} - \frac{1}{2n}.
$$

Simple induction. Base case $n = 0$ and substitute the $n = k$ case into $n = k+1$ and notice $\frac{1}{2k+2}-\frac{1}{k+1} = -\frac{1}{2k+2}$


12. Prove that $|\sin(nx)| \leq n |\sin(x)|$ for any real number $x$ and positive integer $n$.

Base case $n = 1$ gives the trivial $|\sin(x)| \leq |\sin(x)|$
assume $|\sin(kx)| \leq k |\sin(x)|$, then $$|\sin(kx+x)| = |\sin(kx)\cos(x)+\cos(kx)\sin(x)|$$ of course, since $cos \leq 1$, we have $$|\sin(kx)\cos(x)+\cos(kx)\sin(x)| \leq |\sin(kx)+\sin(x)| \leq (k+1)|\sin(x)|$$ with the final simplification following from teh inductive hypothesis.

  
13. Prove that for any real numbers $x_1, x_2, \dots, x_n$, $n \geq 1$, $$
|\sin x_1| + |\sin x_2| + \cdots + |\sin x_n| + |\cos(x_1 + x_2 + \cdots + x_n)| \geq 1.
$$
base case ($n == 1$):
$$|\sin x_1|+|\cos x_1| = \sqrt{\sin^2x_1+\cos^2x_1+2|\sin x_1| |\cos x_1}| \geq 1$$
then, assume $|\sin x_1| + |\sin x_2| + \cdots + |\sin x_k| + |\cos(x_1 + x_2 + \cdots + x_k)| \geq 1.$

we want $|\sin x_1| + |\sin x_2| + \cdots + |\sin x_{k}|+ |\sin x_{k+1}| + |\cos(x_1 + x_2 + \cdots + x_k+x_{k+1})| \geq 1$, and since we assumed the $n = k$ case is true, we only need to prove that $$|\sin x_{k+1}| + |\cos(x_1 + x_2 + \cdots + x_k+x_{k+1})| \geq |\cos(x_1 + x_2 + \cdots + x_k+x_{k})|$$and for simplicity we rename the variables such that we want to prove $$|\sin a| + |\cos b| \geq |\cos(b-a)| = |\cos(b) \cos(a) + \sin(b) \sin(a)|$$
Of course, $|\cos(b) \cos(a) + \sin(b) \sin(a)| \leq |\sin a| + |\cos b|$, completing the proof.

14. Prove that $3^n \geq n^3$ for all positive integers $n$.

straightforward induction. reduce to polynomials and compare.

>[!problem] 15. Let $n \geq 6$ be an integer. Show that 
>$$
\left( \frac{n}{3} \right)^n < n! < \left( \frac{n}{2} \right)^n.
$$


Assume $(\frac{k}{3})^k < k!$
We want to show $(\frac{k+1}{3})^{k+1} < (k+1)!$
But when we substitute $(\frac{k}{3})^k$ into $k!$, the right hand side becomes SMALLER
In other words $(k+1)(\frac{k}{3})^k<(k+1)!$ , so we can't be so sure its greater than $(\frac{k+1}{3})^{k+1}$ just by "using the inductive hypothesis"


>[!problem] 16. Let $n$ be a positive integer. Prove that
>$$
1 + \frac{1}{2^3} + \frac{1}{3^3} + \cdots + \frac{1}{n^3} < \frac{3}{2}.
$$

17. Prove that for any positive integer $n$ there exists an $n$-digit number that is
	(a) divisible by $2^n$ and containing only the digits $2$ and $3$
	(b) divisible by $5^n$ and containing only the digits $5, 6, 7, 8, 9$



18. Prove that for any $n \geq 1$, a $2^n \times 2^n$ checkerboard with $1 \times 1$ corner square removed can be tiled by trominos (3 blocks in an L shape - search it up!)

For $2^1 \times 2^1$ the checkerboard is clearly tiled. Then, assume a $2^k \times 2^k$ checkerboard can be tiled with trominos. Combine four checkerboards of size $2^k\times 2^k$ in a certain rotation where the induction is clear as a tromino shape forms in the middle.

19. Given a sequence of integers $x_1, x_2, \dots, x_n$ whose sum is $1$, prove that exactly one of the cyclic shifts $$ x_1, x_2, \dots, x_n; \quad x_2, \dots, x_n, x_1; \quad \dots; \quad x_n, x_1, \dots, x_{n-1} $$ has all of its partial sums positive. (By a partial sum, we mean the sum of the first $k$ terms, $k \leq n$). 
20. Let $x_1, x_2, \dots, x_n, y_1, y_2, \dots, y_m$ be positive integers, $n, m > 1$. Assume that $x_1 + x_2 + \dots + x_n = y_1 + y_2 + \dots + y_m < mn$. Prove that in the equality $$ x_1 + x_2 + \dots + x_n = y_1 + y_2 + \dots + y_m $$ one can suppress some (but not all) terms in such a way that the equality is still satisfied. 
21. Prove that any function defined on the entire real axis can be written as the sum of two functions whose graphs admit centers of symmetry. 
22. Prove that for any positive integer $n \geq 2$ there is a positive integer $m$ that can be written simultaneously as a sum of $2, 3, \dots, n$ squares of nonzero integers.
