---
title: AMC Prep
author: Ritoban Roy-Chowdhury
date: 17 January 2020
numbersections: true
fontfamily: TheanoModern
---

# 2010 AMC 12B Problem 11

A palindrome between $1000$ and $10,000$ is chosen at random. What is the probability that it is divisible by $7$?

$$\textbf{(A)}\ \dfrac{1}{10} \qquad \textbf{(B)}\ \dfrac{1}{9} \qquad \textbf{(C)}\ \dfrac{1}{7} \qquad \textbf{(D)}\ \dfrac{1}{6} \qquad \textbf{(E)}\ \dfrac{1}{5}$$

## Solution

We are interested in four digit palindromes (10,000 is not a palindrome, and there are no other 5 digit numbers in the range). Notice that such a number is of the form $abba$ -- in other words, this is an "outer number", $a$, and an inner nunmber, $b$. 

Because the outer number $a$ cannot be zero (because then it would be less than 1000), there are 9 choices for it (the digits 1 through 9, inclusive). On the other hand, there are 10 choices for the inner number $b$, so there's a total of 90 palindromes between 1000 and 10,000.

Now, write the palindrome $abba$ as 

$$ 10^3a + 10^2b + 10b + a. $$

We want to calculate the number of possible choices of $a$ and $b$ such that this is divisble by 7. 

$$ 10^3a + 10^2b + 10b + a \equiv 0 \mod 7. $$

Factor. 

$$ 1001a + 110b \equiv 0 \mod 7 $$

Finally, _just know_ that the prime factorization of $1001 = 7 \times 11 \times 13$ and $110 = $5 \times 11 \times 12$. 

$$ (7\cdot11\cdot13)a + (5\cdot11\cdot12)b \equiv 0 \mod 7 $$

Since the $a$ term will always have a factor of 7, there are two cases where the overall expression is divisible by 7.

1. When $b = 0$, because the LHS of the congruence reduces to $(7\cdot11\cdot13)a$, which is always divisble by 7. This is the sequence of palindromes $1001, 20002, 3003, \dots$.  There are 9 possible values, because as we established earlier, there are 9 choices for $a$. 
2. When $b = 7$. Because the first term is always divisible by 7, for the entire expression to be divisible by 7, second term must also have a factor of 7. This is only possible when $b = 7$, leading to another 9 possible palindromes, one for each choice of $a$. 

Therefore, in total, there are $9 + 9 = 18$ palindromes divisible by 7 between 1000 and 10,000, so the answer is $\frac{18}{90} = \frac{1}{5}$, **(E)**.

# 2010 AMC 12B Problem 12

For what value of $x$ does

$$ \log_{\sqrt{2}}\sqrt{x}+\log_{2}{x}+\log_{4}{x^2}+\log_{8}{x^3}+\log_{16}{x^4}=40? $$

$$\textbf{(A)}\ 8 \qquad \textbf{(B)}\ 16 \qquad \textbf{(C)}\ 32 \qquad \textbf{(D)}\ 256 \qquad \textbf{(E)}\ 1024$$

## Solution

This is a straightforward application of the change-of-base formula. 


```{=tex}
\begin{align*}
 \log_{\sqrt{2}}\sqrt{x} + \log_2x + \log_4(x^2) + \log_8(x^3) + \log_{16}(x^4)  &= 40  \\
 \frac{1}{2} \frac{\log_2x}{\log_2\sqrt{2}} + \log_2x + \frac{2\log_2x}{\log_24} + \frac{3\log_2x}{\log_28} + \frac{4\log_2x}{\log_216}  &= 40 \\
 \log_2x + \log_2x + \log_2x + \log_2x + \log_2x &= 40  \\
 5\log_2x &= 40  \\
 \log_2x &= 8 \\
 x &= 256 \qquad \textbf{(D)} \\
\end{align*}
```

# 2010 AMC 12B Problem 13

In $\triangle ABC$, $\cos(2A-B)+\sin(A+B)=2$ and $AB=4$. What is $BC$?

$\textbf{(A)}\ \sqrt{2} \qquad \textbf{(B)}\ \sqrt{3} \qquad \textbf{(C)}\ 2 \qquad \textbf{(D)}\ 2\sqrt{2} \qquad \textbf{(E)}\ 2\sqrt{3}$

## Solution
Because $\cos$ and $\sin$ can never be greater than 1, for them to add up to 2, they must both be exactly 1.

\begin{align*}
\cos(2A-B) &= 1 \\
\sin(A+B) &= 1 \\
\end{align*}

Instead of being stupid like me and trying to expand these out with sum and difference formulas, you can  just directly solve for the angles now. $\arccos{(1)} = 0$ and $\arcsin{(1)} = \frac{\pi}{2}$, so

\begin{align*}
2A-B &= 0 \\
A+B &= \frac{\pi}{2} \\
\end{align*}

Solving the system of equations,

\begin{align*}
2A-B &= 0 \\
   2A &= B \\
A+B &= \frac{\pi}{2} \\
3A &= \frac{\pi}{2} \\
A &= \frac{\pi}{6} = 30^{\circ} \\
B &= 2A = 60^{\circ} \\
C &= 90^{\circ} \\
\end{align*}

This is a $30-60-90$ triangle. Since $AB \text{(the side opposite $C$, the $90^{\circ}$ angle)} = 4$, $AC = 2$, and $BC = 2\sqrt{3}$ **(E)**.


