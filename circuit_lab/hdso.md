---
title: HDSO Circuit Analysis
author: Ritoban Roy-Chowdhury
date: \today
---

$$
\frac{v_{5}-v_{2}}{20 \Omega}+\frac{v_{5}}{10 \Omega}+\frac{v_{5}-v_{4}}{16 \Omega}=0
$$
(1)
$$
\frac{v_{4}-v_{5}}{16 \Omega}+\frac{v_{4}}{160 \Omega}+\frac{v_{4}-v_{3}}{20 \Omega}=0
$$
(2)
$$
\frac{v_{3}-v_{4}}{20 \Omega}+\frac{v_{3}}{30 \Omega}=0
$$
(3)
Plugging into Wolram Alpha (see next page):
$$
v_{3}=-1.25 \quad v_{4}=-2.09 \quad v_{5}=-2.97
$$

Solving the node equations for $\# 9$
Rearrange
(3)
$$
\begin{array}{l}
\frac{v_{3}-v_{4}}{20 \Omega}+\frac{v_{3}}{30 \Omega}=0 \\
v_{3}\left[\frac{1}{20}+\frac{1}{30}\right]+v_{4}\left[-\frac{1}{20}\right]=0 \\
v_{3}=\frac{v_{4}}{20}\left(\frac{1}{20}+\frac{1}{30}\right)=\frac{v_{4}}{2 \theta} \cdot 1^{3} 2=\frac{3}{5} v_{4}
\end{array}
$$
Substitute into
(2)
$$
v_{3}\left[-\frac{1}{20}\right]+v_{4}\left[\frac{1}{16}+\frac{1}{160}+\frac{1}{20}\right]+v_{5}\left[-\frac{1}{16}\right]=0
$$
\& Rearrange
$$
\begin{array}{l}
-\frac{3}{5} \frac{v_{4}}{20}+v_{4} \cdot \frac{19}{160}+\frac{-v_{5}}{16}=0 \\
v_{4}\left[\frac{19}{160}-\frac{3}{100}\right]=\frac{v_{5}}{16} \\
v_{4}=\frac{50}{71} v_{5}
\end{array}
$$
$$
\begin{array}{l}
v_{5}=-2.97 \mathrm{~V} \\
v_{4}=-2.09 \mathrm{~V} \\
v_{3}=-1.25 \mathrm{~V}
\end{array}
$$

10. A continuation of #9. Skip (d), we'll come back to it.
$$
\begin{array}{l}
\text { (e) } i_{R_{1}}=\frac{v_{5}-v_{2}}{R_{1}}=\frac{(-2.97 \mathrm{~V})-(-10 \mathrm{~V})}{20 \Omega}=0.35 \mathrm{~A}=350 \mathrm{~mA} \\
\text { (f) } P_{R_{7}}=i_{R_{7}}^{2} \cdot R_{7}
\end{array}
$$
$$
\begin{array}{l}
\qquad \begin{aligned}
V_{\text {out }}=v_{4}\left(\frac{P_{6}}{R_{6}+R_{7}}\right) &=-2.97 \mathrm{~V}\left(\frac{10 \Omega}{160 \Omega}\right) \\
&=-0.1856 \mathrm{~V} \\
\therefore P_{R_{7}} &=\left(\frac{-2.97-(-0.1856)}{150 \Omega}\right)^{2} \cdot 150 \Omega \\
&=0.0255 \mathrm{~W} \\
&=26 \mathrm{~mW}
\end{aligned}
\end{array}
$$


(d) The equivalent resistance is whatever the resistance "appears" to the voltage source, i.e. the current through the source divided by its voltage.

Since $R_{1}$ and the source are connected in series, the current
$$
i_{S}=i_{R_{5}}=\frac{v_{5}-v_{2}}{20 \Omega}=\frac{(-2.97)-(-10 \mathrm{v})}{20 \Omega}=0.3515 \mathrm{~A}
$$

$$
R_{eq}=\frac{10 V}{0.3515 A}=28.44 \Omega=28 \Omega
$$

## Alt. Using Matrices to solve the node equations

(1) $\mathrm{O}v_{3}+\left[\frac{1}{20}+\frac{1}{10}+\frac{1}{16}\right] v_{5}+\left[-\frac{1}{16}\right] v_{4}=-\frac{1}{2}$
(2) $\left[-\frac{1}{20}\right] v_{3}+\left[-\frac{1}{16}\right] v_{5}+\left[\frac{1}{16}+\frac{1}{100}+\frac{1}{80}\right] v_{4}=0$
(3) $\left[\frac{1}{20}+\frac{1}{30}\right] v_{3}+O v_{5}+\left[-\frac{1}{20}\right] v_{4}=0$
$$

$$
\begin{array}{l}
{\left[\begin{array}{ccc}
0 & -1 / 16 & 17 / 80 \\
-1 / 20 & +19 / 160 & -1 / 16 \\
1 / 12 & -1 / 20 & 0
\end{array}\right]\left[\begin{array}{c}
v_{3} \\
v_{4} \\
v_{6}
\end{array}\right]=\left[\begin{array}{c}
-1 / 2 \\
0 \\
0
\end{array}\right]} \\
v_{3}=-1.25 \mathrm{~V} \quad v_{4}=-2.09 \mathrm{~V} \quad v_{5}=-2.97 \mathrm{~V}
\end{array}
$$

\end{document}

## Question 11
$$
\begin{array}{l}
\text { (1) } \frac{v_{1}-v_{3}}{1.5 k}+\frac{v_{1}-(-5 v)}{1.6 k}=0 \\
\text { (2) } \frac{v_{3}-v_{1}}{1.5 k}+\frac{v_{3}}{6.3 k}-5 m A=0 \\
v_{2}=v_{R_{4}}=(-5 m A)(0.500 k \Omega)=-2.5 V \\
\text { Rearrange (1) } \\
\qquad \begin{aligned}
v_{1} &=\frac{-5}{1600}+\frac{v_{3}}{1000} \\
\frac{1}{1500}+\frac{1}{1600}
\end{aligned}
\end{array}
$$

$$
\begin{aligned}
&\text { Substitute into (2) \& Solve: } v_{3}=7.037 \mathrm{~V}\\
&\begin{array}{l}
\quad v_{1}=1.213 \mathrm{~V} \\
\text { (a) } v_{12}=v_{2}-v_{1}=(-2.5 v)-(1.213 \mathrm{~V}) \\
=-3.71 \mathrm{~V}
\end{array}\\
&\approx 4 V\\
&\text { (b) } i_{R 1}=\frac{v_{3}}{R_{1}}=\frac{7.037 V}{6.3 k \Omega}=1.117 \mathrm{~mA}\\
&\approx \operatorname{l} mA
\end{aligned}
$$

## Alternate solution #11
