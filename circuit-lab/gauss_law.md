---
title: Gauss's Law
author: Ritoban Roy-Chowdhury
geometry: margin=1in
header-includes:
    - \usepackage[per-mode=fraction]{siunitx}
    - \usepackage{graphicx}
    - \usepackage{physics}
---

# Equations


Gauss' Law gives us a very natural way to compute the electric field in more complicated situations. First, we must define flux.

```{=tex}

\begin{equation}
\label{eq:defn-flux}
\Phi = \oint \va{E} \cdot d\va{A}.
\end{equation}

```

Flux is the sum, at every point on the surface $d\va{A}$ is the normal vector, of the dot product $\va{E} \cdot d\va{A}$. The dot product tells you how much two vectors point in the same direction. The magnitude of flux is $\Phi = (E \cos \theta)A$. If the two vectors point in the same direction, $\theta = 0$, $\cos \theta = 1$, so the flux is large. Therefore, you can think of the flux as how much the electric field "pierces" a surface at any given point.

Gauss' law tells you that 

```{=tex}
\begin{equation}
\label{eq:gauss-law}
\varepsilon_0 \Phi = q_{enc}.
\end{equation}
```

```{=tex}
This says, for any Gaussian surface (that's just an arbitrary surface we introduce), the charge that surface encloses \(q_{enc}\) is proportional to the flux through the surface $\Phi$. So if a Gaussian surface contains a positive charge, the electric field will point away from it, so the flux will be a large positive number. Even if the Gaussian surface is within an electric field because of charges outside of the Gaussian surface, since there are no charges inside the surface, all of the electric field lines will simply pass through the surface, entering on one side and leaving out the other, so the total flux will be zero.
```

An alternative form of Gauss' law is 

```{=tex}

\begin{equation}
\label{eq:alt-gauss-law}
\Phi = \oint \va{E} \cdot d\va{A} = \frac{q_{enc}}{\varepsilon_0}
\end{equation}

```

Unfortunately, we cannot usually solve this surface integral directly. Therefore, we instead have to utilize the symmetry of a situation to find an analytic solution. I'll include one example here. 

```{=tex}
Consider the case of a line of infinite charge. The electric field around this line will always point radially outwards. Therefore, a useful Gaussian surface might be a cylinder, surrounding the line. The electric field would only graze the endcaps of the cylinder, so that wouldn't contribute to the flux. On the other hand, along the curved portion, the electric field points in the same direction as the surface normal \(d\va{A}\), so the dot product is simply \( E dA \cos 0 = E dA \).

Pulling the E out of the integral, we get

\[ \Phi = \oint E dA = E \oint dA. \]

\(\oint dA \) is just the surface integral over A, which is just the surface area of the curved portion of the cylinder, which is just \( 2 \pi r h \), so 

\[ \Phi = E(2 \pi r h). \]

Substituting into Gauss' Law (Eqn. \ref{eq:guass-law}), we get


\[ \varepsilon_0 E(2 \pi r h) = q_{enc}. \]

Normally, we aren't given the charge \(q_{enc}\), but we do have the charge density \(\lambda\), so that \( q_{enc} = \lambda h \). Substituting, we get 


\[ \varepsilon_0 E(2 \pi r h) = \lambda h, \]

which, after cancelling \(h\) and dividing by \(2\pi r \varepsilon_0\), yields

\begin{equation}
\label{eq:electric-field-line-of-charge}
E = \frac{\lambda}{2 \pi \varepsilon_0 r}.
\end{equation}

This is the magnitude of the electric field \(\va{E}\), as a result of an infinite line of charge with charge density \(\lambda\), at some distance \(r\) away from the line.

Note that the electric field decreases with \(r\), not \(r^2\). This is because the line is infinite in the y direction, so it's only spreading out in the 2D plane, the curved side of the cylinder.
```


Following a similar procedure, we find that the electric field due to an infinite non-conducting sheet with uniform surface charge density $\sigma$ is perpendicular to the sheet and has magnitude 

```{=tex}

\begin{equation}
\label{eq:electric-field-infinite-sheet}
E = \frac{\sigma}{2 \varepsilon_0}.
\end{equation}

```

Note that this has _no depedence_ on how far away the point is from the sheet. This is because all of the lines are parallel, they don't spread out at all, and the plane is infinite. Additionally, note that the electric field in each direction is divided by 2, because intuitively, half the charge is going one way, and half the charge is going the other, so you have one $\va{E}$ acting in each direction.

```{=tex}
Additionally, you can show that for a uniform sphereical shell of charge with total charge \(q\), inside the shell, \( E = 0 \). Outside the shell, E is directed radially,

\begin{equation}
\label{eq:electric-field-outside-spherical-shell}
E = \frac{1}{4 \pi \varepsilon_0} \frac{q}{r^2} \qquad (\text{for } r \geq R).
\end{equation}

This is equivalent to if the entire charge were located at the center of the sphere.
```

```{=tex}

Inside a uniform sphere of charge, with charge $q$ and radius $R$, at a distance $r$ from the center the electric field is also radially outward and has magnitude 


\begin{equation}
\label{eq:electric-field-inside-uniform-sphere}
E = \left( \frac{q}{4 \pi \varepsilon_0 R^3} \right) r.
\end{equation}

```


Finally, note that on an isolated conductor, at electrostatic equilibrium, any charge will _always_ be on the surface. Intuitively, this is because all the charges are trying to get away from each other. But formally, this is because if you were to draw a Gaussian surface right underneath the surface, there would not be an electric field inside it (a conductor just sitting on a table doesn't have current flowing through it, but we know all conductors have free electrons which would be moved by such an electric field), so by Gauss' law, since there's no electric field, there must not be any charges.

This is _NOT_ true for a non-conductive surface, where it is entirely possible for the charges to be dispersed throughout the surface.

# Problems

## Question 1 (Resnick-Hallidy, Ch. 23, P1)
```{=tex}
An infinite line of charge produces a field of magnitude \SI{1.7e-4}{\newton\per\coulomb} at distance 9.0 m. Find the field magnitude at distance 2.0 m.
```

### Solution
```{=tex}
This is simple application of the electric field due to a line of charge formula (Eqn. \ref{eq:electric-field-line-of-charge}). 

Let's rearrange it to deal with the electric field 2 positions, \( E_1 \) and \(E_2\)

\[ E_1 = \frac{\lambda}{2 \pi \varepsilon_0 r_1} \]
\[ E_2 = \frac{\lambda}{2 \pi \varepsilon_0 r_2} \]

Rearrange to isolate \(\lambda\), since that's the same between the two equations.

\[ \lambda = E_1(2 \pi \varepsilon_0 r_1) \]

Substitute into the second equation.

\[ E_2 = \frac{E_1(2 \pi \varepsilon_0 r_1)}{2 \pi \varepsilon_0 r_2} \]

Cancel. 

\[ E_2 = \frac{E_1 r_1)}{r_2} \]

And substitute,

\[ E_2 = \frac{\SI{1.7e4}{\newton\per\coulomb} (\SI{9.0}{m}))}{\SI{2.0}{m}} = \SI{7.7e4}{\newton\per\coulomb}. \]

```

## Question 2 (Resnick-Halliday, Ch. 23, P3)
An unknown charge sits on a conducting solid sphere of radius 10 cm. If the electric field 30 cm from the center of the sphere has the magnitude 3.0 10 3 N/C and is directed radially inward, (a) what is the net charge on the sphere? and (b) what is the charge density?

### Solution (a)

Lets start with Gauss' law (Eqn. \ref{eq:alt-gauss-law}),

```{=tex}
\[ \Phi = \oint \va{E} d\va{A} = \frac{q_{enc}}{\varepsilon_0} \]

It's a sphere, so we can factor out the \(\va{E}\) and use the surface area to calcluate the surface integral,

\[ \Phi = \va{E}(4 \pi r^2)  = \frac{q_{enc}}{\varepsilon_0} \]

\[ E = \frac{1}{4\pi\varepsilon_0} \frac{q_{enc}}{r^2} \]

It says ``unkown charge'', so lets try and solve for that. They give us the value of the electic field at 30 cm, so lets substitute that.

\[ \SI{-3.0e3}{\newton\per\coulomb} = \frac{1}{4\pi\varepsilon_0} \frac{q_{enc}}{(\SI{0.30}{m})^2} \]

\[ q_{enc} = \SI{-3.00e-4}{\coulomb} \]

```

### Solution (b)

Part B asks for the charge density, so you just divide by the surface area of the actual sphere (using the 10 cm). 

```{=tex}

\[ \sigma = \frac{q_{enc}}{4 \pi r^2} = \frac{\SI{-3.00e-8}{\coulomb}}{4 \pi (\SI{0.10}{cm})^2} = \SI{-2.39e-7}{\coulomb\per\meter\squared} \]

```

## Question 3 (Resnick-Halliday, Ch. 23, P5)
An isolated conductor has net charge $\SI{+10e-6}{\coulomb}$ and a cavity with a particle of charge $q = \SI{-4.0e-6}{\coulomb}$. What is the charge on (a) the cavity wall and (b) the outer surface?

### Solution (a)
This problem is actually a lot simpler that it seems. Recall that on a conductor, all charges will lie at the surface -- in this case, that may be the outer surface or the inner surface of the cavity. So the answers to part (a) and (b) should add to \SI{+10e-6}{\coulomb}.

Now, consider a Gaussian surface completely enclosing the cavity. The net electric field along this surface should be zero, because otherwise, there would be a current. Therefore, the charge on the inside cavity wall is teh same as the charge of the particle, $\SI{+4.0e-6}{\coulomb}$.

### Solution (b)
Therefore, the rest of the charge must come from the outer surface, with a charge of $\SI{+6.0e-6}{\coulomb}$.

## Question 4 (Resnick-Halliday, Ch. 23, P7)
In Fig. 23-24, two large, thin metal plates are parallel and close to each other. On their inner faces, the plates have excess surface charge densities of opposite signs and magnitude $\SI{2.31e-22}{\coulomb\per\meter\squared}$. In unit-vector notation, what is the electric field at points (a) to the left of the plates, (b) to the right of them, and (c)

### Solution (a)
Like the previous one, this one is also a lot simpler that it looks. Because they are infinite plates, the electrical field is constant. Since the charge density of the positive and negative charges is the same, they cancel out on the left, so the electric field is 0. 

### Solution (b)
For the same reason as (a), the electric field to the right is 0.

### Solution (c)
Between the plates, the field will go from the positive to the negative. The strength of the field is given by Eqn. \ref{eq:electric-field-infinite-sheet}, except without dividing by 2 (because there's both a positive and a negative charge, so the 2s cancel).

```{=tex}
\[ \va{E} = -\frac{q}{\varepsilon_0} = -\frac{\SI{2.31e-22}{\coulomb\per\meter\squared}}{\varepsilon_0} = (\SI{-2.61e-11}{\newton\per\coulomb})\hat{i} \]

It's \(\hat{i}\) and negative because they wanted it in unit-vector notation, and the field is pointing in the -x direction.
```

## Question 5 (Resnick-Halliday, Ch. 23, P9)
In Fig. 23-26, a nonconducting spherical shell of inner radius $a = 1.50$ cm and outer radius $b = 2.40$ cm has (within its thickness) a positive volume charge density $\rho = A/r$, where $A$ is a constant and $r$ is the distance from the center of the shell. In addition, a small ball of charge $q = \SI{75.0}{\femto\coulomb}$ is located at that center.  What value should A have if the electric field in the shell ($a \leq r \leq b$) is to be uniform?

### Solution

Let's begin by creating a Gaussian sphere centered at $q$ with radius $s$. The charge within the spherical shell from $a \leq r \leq s$ is 

```{=tex}
\[ q_{shell} = \int _a ^s \rho dV, \]

by the definition of charge density. Since the volume of a sphere is \( V = \frac 4 3 \pi r^3 \), \( dV = 4 \pi r^2  dr \). Substituting, 

\[ q_{shell} = \int _a ^s \frac{A}{r} 4 \pi r^2 \dd{r}. \]

Cancelling $r$ and evaluating the integral, we get,

\[ q_{shell} = 4 \pi A \left[ \frac{r^2}{2} \right]_a ^s.  \]

Simplify to get 

\[ q_{shell} = 2 \pi A \left[ s^2 - a^2 \right].  \]

Thus, the total charge \(q_{enc}\) is 

\[ q_{enc} = q + q_{shell} = \SI{75.0}{\femto\coulomb} + 2 \pi A \left[ s^2 - a^2 \right] \]


Let's now bring in Gauss' Law (Eqn. \ref{eq:alt-gauss-law}, rearranged slightly).

\[ \Phi = q_{enc} = \varepsilon_0 \oint \va{E} \cdot d\va{A} \]

Because we're dealing with spheres, the electric field is symmetic, we can take E out of the integral and use the surface area to solve the surface integral, as we did in Eqn. \ref{eq:electric-field-outside-spherical-shell}.

\[ \Phi = q + 2 \pi A (s^2 - a^2)  = \varepsilon_0(E \cdot 4 \pi s^2). \]

Since we want to find out when \(\va{E}\) is uniform (a.k.a when \(E\), the magnitude of \(\va{E}\), is constant), Lets divide both sides by \( 4 \pi \varepsilon_0 s^2 \) to isolate \(E\).

\[ E = \frac{q}{4\pi\varepsilon_0 s^2} + \frac{2\pi A s^2}{4\pi\varepsilon_0 s^2} - \frac{2 \pi A a^2}{4\pi\varepsilon_0 s^2}. \]

CAncelling the \(s^2\) from the middle term,

\[ E = \frac{q}{4\pi\varepsilon_0 s^2} + \frac{2\pi A}{4\pi\varepsilon_0} - \frac{2 \pi A a^2}{4\pi\varepsilon_0 s^2}, \]

reveals that only the first term and the last term vary with respect to \(s\). The middle term is constant. Since we want \(E\) to be constant, the remaining term 1 and term 3 should cancel each other out, 


\[ \frac{q}{4\pi\varepsilon_0 s^2} = \frac{2 \pi A a^2}{4\pi\varepsilon_0 s^2}. \]

Convieniently, \( 4\pi\varepsilon_0 s^2 \) cancels (which makes sense. Otherwise, there wouldn't be any way for \(E\) to be constant), and it simplifies to 

\[ q = 2 \pi A a^2 \]
\[ A = \frac{q}{2 \pi a^2} = \frac{\SI{75.0e-15}{\coulomb}}{2 \pi \SI{1.50e-2}{m}} = \SI{5.30e-11}{\coulomb\per\meter\squared}. \]


```
