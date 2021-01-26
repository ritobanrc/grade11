---
title: AMC Prep
author: Ritoban Roy-Chowdhury
date: 17 January 2020
numbersections: true
fontfamily: TheanoModern
---

# 2010 AMC 12A Problem 17

Bernardo randomly picks 3 distinct numbers from the set $\{1,2,3,4,5,6,7,8,9\}$ and arranges them in descending order to form a 3-digit number. Silvia randomly picks 3 distinct numbers from the set $\{1,2,3,4,5,6,7,8\}$ and also arranges them in descending order to form a 3-digit number. What is the probability that Bernardo's number is larger than Silvia's number?

$$ \textbf{(A)}\ \frac{47}{72} \qquad \textbf{(B)}\ \frac{37}{56} \qquad \textbf{(C)}\ \frac{2}{3} \qquad \textbf{(D)}\ \frac{49}{72} \qquad \textbf{(E)}\ \frac{39}{56} $$

## Solution

Consider the following cases.

1. If Bernardo picks a 9, his number will always be greater than Silvia's. The probability of this is 

$$ \frac 1 9 + \frac 8 9 \cdot \frac 1 8 + \frac 7 9 \cdot \frac 1 7 = \frac 3 9 = \frac 1 3.$$

2. If Bernardo does _not_ pick 9 ($\frac 2 3$), both Bernardo and Silvia are picking from the same set of numbers ($\{1 ..8\}$), so it may be tempting to say that the probability of one being greater than the other is exactly $\frac 1 2$. This would be on the right track, HOWEVER, it doesn't account for the possibility that they pick the same number. 

    a. Since they are each choosing 3 numbers out of 8, and order doesn't matter, the number of possible numbers they can choose is 

    $$ \binom{8}{3} = \frac{8!}{3! \cdot 5!} = \frac{8 \cdot 7 \cdot 6}{6} = 56.$$

    b. Then the probability that they choose the same number is just $\frac 1 56$ (i.e. Bernardo can choose any number, there's a $\frac{1}{56}$ chance that Silvia choose the same number, or vice versa).

    c. Then, to the probabilty that either one is greater than the other, we find 1 minus the probability that they are both the same (the probability that they are different), and then divide that by 2 (the probability that Bernardo specifically is greater).

    $$ \frac{1 - \frac{1}{56}}{2} = \frac{55}{112} $$.

Adding these two cases together,

$$ \frac 1 3 + \frac 2 3 \times \frac{55}{112} = \frac 1 3 + \frac 1 3 \times \frac{55}{56} = \frac 1 3 \left(1 + \frac{55}{56}\right) = \frac 1 3 \times \frac{111}{56} = \frac{37}{56} $$.

Therefore, the answer is **(B) $\frac{37}{56}$**. 

## Key Insight

The probability of $X > Y$ is the same as the probability of $Y > X$ if $X$ and $Y$ are chosen from the same distribution. You can find this probability by removing the probability that $X = Y$ and dividing by 2.



# 2010 AMC 12A Problem 18

A 16-step path is to go from $(-4,-4)$ to $(4,4)$ with each step increasing either the $x$-coordinate or the $y$-coordinate by 1. How many such paths stay outside or on the boundary of the square $-2 \le x \le 2$, $-2 \le y \le 2$ at each step?

$$\textbf{(A)}\ 92 \qquad \textbf{(B)}\ 144 \qquad \textbf{(C)}\ 1568 \qquad \textbf{(D)}\ 1698 \qquad \textbf{(E)}\ 12,800$$

## Solution

Nothing much to this problem, just chug through the numbers until you get **(C) $1698$**. There are more elegant ways to do this with combinatorics, but it's a number 18, I can do some arithmetic at this point.

# 2010 AMC 12A Problem 19

Each of $2010$ boxes in a line contains a single red marble, and for $1 \le k \le 2010$, the box in the $k\text{th}$ position also contains $k$ white marbles. Isabella begins at the first box and successively draws a single marble at random from each box, in order. She stops when she first draws a red marble. Let $P(n)$ be the probability that Isabella stops after drawing exactly $n$ marbles. What is the smallest value of $n$ for which $P(n) < \frac{1}{2010}$?

$$\textbf{(A)}\ 45 \qquad \textbf{(B)}\ 63 \qquad \textbf{(C)}\ 64 \qquad \textbf{(D)}\ 201 \qquad \textbf{(E)}\ 1005$$

## Solution

Since the $n$-th box contains 1 red marble, and $n$ white marbles, for a total of $n + 1$ marbles. Isabella stops after drawing $n$ marbles if and only if she draws a white marble from every single box, all the way up until the last one, where she draws a red marble. The probability of this is

$$ P(n) = \frac 1 2 \cdot \frac 2 3 \cdot \frac 3 4 \cdot \dots \cdot \frac{n - 1}{n} \cdot \frac{1}{n + 1}. $$

Notice that the second-last term has a denominator of $n$ -- because there are $n$ balls in the $n-1$-th box, and $n-1$ of those are white, and $1$ is red. The last term is $\frac{1}{n + 1}$ because there is only 1 red ball (the stopping condition) and the $n$-th box has $n + 1$ balls total.

Notice that everything cancels, leaving, 

$$ P(n) = \frac{1}{n} \cdot \frac{1}{n + 1} = \frac{1}{n(n + 1)}. $$

The problem asks for when $P(n) < \frac{1}{2010}$, so let's substitute

```{=tex}
\begin{align*} 
P(n) &<  \frac{1}{2010} \\ 
\frac{1}{n(n+1)} &< \frac{1}{2010} \\ 
n(n+1) &>  2010.
\end{align*}
```

Some quick experimentation reveals that $44 \times 45 = 1980$ and $45 \times 46 = 2070$, so the answer is **(A) 45**.
