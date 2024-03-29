---
title: Three ways used to represent a numerical semigroup
authors:
  - name: Pedro A. García Sánchez
    affiliations:
      - Universidad de Granada
---


A numerical semigroup is a subset of the set of nonnegative integers (denoted
here by $\mathbb{N}$) closed under addition, containing the zero element and with
finite complement in $\mathbb{N}$. Observe that a numerical semigroup is a commutative
monoid, thus is somehow surprising that it is required that zero belongs to
the set under consideration. Some authors use the term numerical monoid to
stress out this property. Note also that up to isomorphism the set of
numerical semigroups classify the set of all submonoids of $(\mathbb{N},+)$. Let $S$
be submonoid of $\mathbb{N}$, the condition of having finite complement in $\mathbb{N}$ is
equivalent to saying that the greatest common divisor ($\gcd$ for short) of
its elements is one.

Numerical semigroups probably where first considered while studying the set of
nonnegative solutions of Diophantine equations. Given positive integers
$a_1,\dots,a_n$ with greatest common divisor one, the set of elements $b\in
\mathbb{N}$ such that $a_1 x_1+\cdots+a_n x_n=b$ has a nonnegative integer solution is
a numerical semigroup. Actually, one of the first known problems related to
numerical semigroups was to determine in terms of $a_1,\dots,a_n$, which is
the largest integer for which there is no nonnegative integer solution. This
is known as the Frobenius problem, since it seems that Frobenius it problem in
one of his lectures.

## Generators (first choice)

The set of integers for which there is a nonnegative integer solution of $a_1x_1+\cdots+ a_nx_n=b$ can be expressed as $\{ a_1 x_1+\cdots+ a_n x_n  :  x_1,\dots,x_n\in \mathbb{N}\}$, or in a more abbreviated notation, as $\langle a_1,\dots,a_n\rangle$. We say that $\{a_1,\dots,a_n\}$ is a system of generators of $S$, or simply, that $\{a_1,\dots,a_n\}$ generates $S$. If no proper subset of $\{a_1,\dots,a_n\}$ generates $S$, then we, as expected, say that $\{a_1,\dots,a_n\}$ is a minimal system of generators of $S$. As $S$ is cancellative ($a+b=a+c$ implies $b=c$), $S$ admits a unique minimal system of generators, say $(S\setminus\{0\})\setminus ((S\setminus\{0\}) + (S\setminus\{0\}))$. The cardinality of the minimal system of generators of $S$ is known as the embedding dimension of $S$ (we will see later why this weird name).

Observe that if $S$ is generated by $\{a_1,\dots,a_n\}$, then $\gcd(\{a_1,\dots,a_n\})=1$ (and that if $\gcd(\{a_1,\dots,a_n\})=1$, then the submonoid of $\mathbb{N}$ spanned by $\{a_1,\dots,a_n\}$ is a numerical semigroup).

### Multiplicity, Frobenius number, Gaps, (Cohen-Macaulay) type

As we mentioned above, Frobenius proposed the problem of finding a formula for the largest integer for which there is no (nonnegative integer) solution to $a_1x_1+\cdots+ a_nx_n=b$. This in our notation is equivalent to say which is the largest integer not in the numerical semigroup $S=\langle a_1,\dots,a_n\rangle$. This is why $\max(\mathbb{Z}\setminus S)$ is known as the Frobenius number of $S$ (here we are using $\mathbb{Z}$ to denote the set of integers). If $g$ is the Frobenius number of $S$, then $g+(\mathbb{N}\setminus \{0\})\subset S$, and in particular $g+(S\setminus \{0\})\subseteq S$. The integers fulfilling this condition are known as pseudo-Frobenius numbers, and its cardinality is the (Cohen-Macaulay) type of $S$.

Given a numerical semigroup $S$, we can define on $\mathbb{Z}$ the following order relation: $a\leq_S b$ if $b-a\in S$. It turns out that the set of pseudo-Frobenius numbers is the set of maximal elements of $\mathbb{Z}\setminus S$ with respect to this ordering.

The positive integers not belonging to $S$ are the gaps of $S$, and its cardinality is sometimes known as the gender of $S$. If $g$ is the Frobenius number of $S$, some authors reserve the word hole for those integers $x$ verifying that $x\not \in S$ and $g-x\not\in S$. Thus every hole is a gap, but the converse needs not to be true.

The least positive integer belonging to a numerical semigroup is its multiplicity. The multiplicity of a numerical semigroup is an upper bound for the embedding dimension of $S$. This is because there cannot be two different minimal generators congruent modulo the multiplicity.

### Apéry sets, the {sc}`Tool`

Recall that two minimal generators of a numerical semigroup cannot be congruent modulo the multiplicity, in fact, they cannot be congruent modulo any nonzero element of the numerical semigroup. In this sense, minimal generators are minimal also with respect to be congruent to any nonzero element of the numerical semigroup. Following this idea for a given numerical semigroup $S$ and a nonzero element $n$ of $S$, we can consider the set $\{w_0,\dots,w_{n-1}\}$ where $w_i$ is the least element in $S$ congruent to $i$ modulo $n$. One can easily see that this set corresponds to the set $\{s\in S :  s-n\not\in S\}$. Apéry was the first exploiting this idea and this is why this set is known as the Apéry set of $n$ in $S$. If $n$ is chosen as the multiplicity of $S$, then sometimes this set is called a standard basis of $S$. Since this set appears everywhere in our approach to the study of numerical semigroups, we introduce the notation $\operatorname{Ap}(S,n)$ to refer to it.

The Apéry set of $n$ in $S$ has some wonderful properties. We enumerate some of them here, but later more will arise.

- Every integer $x$ can be expressed uniquely as $x=k n+w$ for some $k\in \mathbb{Z}$ and $w\in \operatorname{Ap}(S,n)$. And $x\in S$ if and only if $k\geq 0$.

- Thus if we want to know if $x$ belongs to $S$, we find $w\in \operatorname{Ap}(S,n)$ such that $x\equiv w \mod n$; then $x\in S$ if and only if $w\leq x$.
- The Frobenius number of $S$ is $\max(\operatorname{Ap}(S,n))-n$.

- More generally, an integer $g$ is a pseudo-Frobenius number of $S$ if and only if $g+n$ is maximal in $\operatorname{Ap}(S,n)$ with respect to $\leq_S$. It follows that the type of $S$ is the cardinality of $\operatorname{Maximals}_{\leq_S}(\operatorname{Ap}(S,n))$.

- By Selmer's formula, the number of gaps equals $\frac{1}n\sum_{w\in\operatorname{Ap}(S,n)}w -\frac{n-1}2$.

Hence the knowledge of the Apéry set of a numerical semigroup $S$ with respect to any of its nonzero elements, solves the membership problem, allows us to know the Frobenius number of $S$, its pseudo-Frobenius numbers (and thus its type) and its gender.

## Fundamental gaps (second choice)

The Frobenius number of $\mathbb{N}$ is $-1$. If $S$ is a numerical semigroup other than $\mathbb{N}$, then the Frobenius number of $S$ is a positive integer, and the same holds for its pseudo-Frobenius numbers, that is, they are gaps of $S$. There are 1,156,012 numerical semigroups with Frobenius number 39. Thus the Frobenius number is not suitable to describe uniquely a numerical semigroup (it can be shown that a numerical semigroup is uniquely determined by its Frobenius number $g$ if and only if $g\in \{-1,1,2,3,4,6\}$). Among these 1,156,012 numerical semigroups, 227 of them have $\{39\}$ as set of pseudo-Frobenius numbers. Hence pseudo-Frobenius numbers are also a bad choice to uniquely describe a numerical semigroup.

Clearly, the set of gaps of $S$ uniquely determines $S$. But in this set a lot of information is redundant, since if $x | y$ (read $x$ divides $y$) and $y$ is a gap of $S$, then $x$ must also be a gap of $S$. Hence among the gaps of $S$ we only need those that are maximal with respect to $|$. These are known as fundamental gaps of $S$, and they uniquely determine $S$. Clearly an integer $x$ is a fundamental gap of $S$ if and only if $x\not\in S$ and $\{2x,3x\}\subset S$.

Let $X$ be a subset of $\mathbb{N}\setminus \{0\}$. Denote by $\operatorname{D}(X)$ the set of positive integers dividing some $x\in X$. If $X$ is the set of fundamental gaps of $S$, then $S=\mathbb{N}\setminus \operatorname{D}(X)$. If $g$ is the Frobenius number of $S$ (observe that this means that $g=\max X$), then 
\begin{equation*} 
    \left\lceil \frac{g}6\right\rceil \leq \# X\leq \left\lceil \frac{g}2\right\rceil.
\end{equation*} 
There are positive integers $g$ for which there is no numerical semigroup not reaching the lower bound, whilst the upper bound is always reached by $\{0,g+1,\to\}$.

### The set of over-semigroups of a numerical semigroup

Minimal generators of a numerical semigroup $S$ can be characterized as those elements $n\in S$ for which $S\setminus\{n\}$ is a numerical semigroup. We could then consider the dual of this property, that is, which are the integers $x\not\in S$ such that $S\cup\{x\}$ is a numerical semigroup? If $S\cup\{x\}$ is a numerical semigroup, then

- $k x\in S$ for every integer $k$ greater than one, or in other words,
$\{2x,3x\}\subset S$, and

- $x+(S\setminus\{0\})\subseteq S$.

Hence $x$ is both a pseudo-Frobenius number and a fundamental gap of $S$. These gaps are known as special gaps of $S$. Thus these are those fundamental gaps that are maximal with respect to $\leq_S$.

By using this idea it is easy to construct the set of all numerical semigroups containing $S$ by adjoining to $S$ each of its fundamental gaps, and then repeat the process for each resulting semigroup until we reach $\mathbb{N}$ (this will happen after a finite number of steps). The key to perform this in an easy way is the following: if $X$ is the set of fundamental gaps of $S$ and $Y$ is the set of fundamental gaps of $S\cup \{x\}$ for some $x\in X$, then 
\begin{equation*}
    Y=(X\setminus\{x\})\cup \left\{ \frac{x}p : p \hbox{ a prime dividing } x \hbox{ and } \frac{x}p\not \in \operatorname{D}(X\setminus\{x\})\right\}.
\end{equation*}

:::{seealso} Example
  Let us consider the semigroup $S=\mathbb{N}\setminus\operatorname{D}(5,6)$. We have that $5$ is
  prime and $6=2\cdot 3$, and both are maximals of $\{5,6\}$ with respect to
  $\leq_S$. Thus our semigroup has two "children"'': $\mathbb{N}\setminus\operatorname{D}(6)$ (by
  removing $5$) and $\mathbb{N}\setminus\operatorname{D}(2,3,5)$ (from the decomposition of $6$).
  Proceeding in this way, we obtain the following graph of inclusions

![](images/diagramad56.svg)
<!--    \centerline{\xymatrix @R=1pc @C=2pc{
        & \mathbb{N}\setminus\operatorname{D}(5,6)\ar[dl]\ar[dr]  &\\
        \mathbb{N}\setminus\operatorname{D}(6)\ar[d] & & \mathbb{N}\setminus\operatorname{D}(2,3,5)\ar[dll]\ar[dl]\ar[d] \\
        \mathbb{N}\setminus\operatorname{D}(2,3)\ar[d]\ar[drr] & \mathbb{N}\setminus\operatorname{D}(2,5)\ar[dl] &
        \mathbb{N}\setminus\operatorname{D}(3,5)\ar[d] \\
        \mathbb{N}\setminus\operatorname{D}(2)\ar[dr] & &\mathbb{N}\setminus\operatorname{D}(3)\ar[dl]\\
        & \mathbb{N}\setminus\operatorname{D}(1)\ar[d] & \\
        & \mathbb{N} &
        }}-->
:::

:::{seealso} Example
  We construct the set of numerical semigroups with Frobenius number eight. They
  all contain the semigroup $\{0,9,10,\to\}=\mathbb{N}\setminus\operatorname{D}(5,6,7,8)$. When adjoining a
  special gap, we will never use 8, so that the Frobenius number is preserved.

![](images/diagramad5678.svg)
<!--  \centerline{
    \xymatrix @R=1.5pc @C=.05pc{
      &  & \mathbb{N}\setminus\operatorname{D}(5,6,7,8)\ar[dll]\ar[d]\ar[drr]  & & \\
      \mathbb{N}\setminus\operatorname{D}(6,7,8)\ar[d]\ar[dr] & &
      \mathbb{N}\setminus\operatorname{D}(3,5,7,8) \ar[dr]\ar[dll]\ar[drr]
      & & \mathbb{N}\setminus\operatorname{D}(5,6,8)\ar[d]\ar[dlll]\\
      \mathbb{N}\setminus\operatorname{D}(3,7,8)\ar[dr] & \mathbb{N}\setminus\operatorname{D}(6,8)\ar[d]
      & &
      \mathbb{N}\setminus\operatorname{D}(5,7,8)\ar[d]   &
      \mathbb{N}\setminus\operatorname{D}(3,5,8)\ar[dlll]\ar[dl]\\
      & \mathbb{N}\setminus\operatorname{D}(3,8) & & \mathbb{N}\setminus\operatorname{D}(5,8) &
      }
    }-->

  Hence there are ten semigroups with Frobenius number eight.
:::

## Presentations (third choice)

Let $S$ be the numerical semigroup generated by $\{2,3\}$. We could think of $S$ as the commutative monoid generated by two elements $x$ and $y$ such that $3x=2y$. This is the idea of a presentation. Let us formalize it. Assume that $S$ is minimally generated by $\{n_1,\dots,n_p\}$. The map
\begin{equation*} 
    \varphi\colon \mathbb{N}^p \to S,\ \varphi(a_1,\dots,a_p)=a_1n_1+\cdots+a_pn_p
\end{equation*}
is a monoid epimorphism, and thus $S$ is isomorphic to $\mathbb{N}^p/\operatorname{Ker} (\varphi)$, where $\operatorname{Ker}(\varphi)=\{ (a,b)\in \mathbb{N}^p\times \mathbb{N}^p  :  \varphi(a)=\varphi(b)\}$. A presentation of $S$ is just a system of generators of $\operatorname{Ker}(\varphi)$ (as a congruence).

Rédei proved that every finitely generated commutative monoid is finitely presented, and thus every numerical semigroup is finitely presented. Moreover, for numerical semigroups the concepts of minimality with respect to cardinality and set inclusion of a presentation coincide.

Rosales gave a procedure to construct a minimal presentation of a numerical semigroup from its minimal system of generators. We describe this method briefly. Assume that $S$ is minimally generated by $\{n_1,\dots,n_p\}$. Let $n\in S$. Associated to $n$ we define a graph $G_n$ whose vertices are
\begin{equation*} 
    V_n=\{ n_i  :  n-n_i\in \mathbb{N}\}
\end{equation*}
and with edges
\begin{equation*} 
    E_n=\{ n_in_j  :  n-(n_i+n_j)\in \mathbb{N}\}.
\end{equation*}
If $G_n$ is connected, then set $\rho_n=\emptyset$. Otherwise, assume that $C_1,\dots,C_k$ are its connected components. For every $i\in\{1,\dots,k\}$ there exists a factorization (expression) of $n$ in which only vertices of $C_i$ appear, or in other words, there exists $\gamma_i\in \varphi^{-1}(n)$ such that the $j$th coordinate of $\gamma_i$ is zero whenever $n_j$ is not a vertex of $C_i$. Set $\rho_n=\{(\gamma_1,\gamma_2),(\gamma_1,\gamma_3),\dots,(\gamma_1,\gamma_k)\}$. Then $\rho=\bigcup_{n\in S} \rho_n$ is a minimal presentation of $S$ (moreover, every minimal presentation can be obtained in this way if we allow in the definition of $\rho_n$ other pairs so that there is a path linking every two different connected components of $G_n$). There are finitely many $n\in S$ for which $G_n$ is not connected. Rosales proved that if $G_n$ is not connected, then $n$ is of the form $n=n_i+w$ with $i\in \{2,\dots,p\}$ and $0\not=w\in\operatorname{Ap}(S,n_1)$.

### Some (numerical) semigroup rings

Let $K$ be a field and $S$ be a numerical semigroup. We choose $t$ to be a symbol. Define $K[S]=\bigoplus_{s\in S} K t^s$ and $K[\![S]\!]=\prod_{s\in S} K t^s$. We will represent the elements $h$ of $K[\![S]\!]$ as $h=\sum_{s\in S} a_s t^s$, with $a_s\in \mathbb{N}$ for all $s$. The element $h$ is in $K[S]$ if and only if $a_s=0$ for almost all $s\in S$ (all but a finite number of them). We can add two elements of $K[\![S]\!]$ (and of $K[S]$) by adding the coefficients componentwise, and we can multiply them by using the distributive law and the rule $t^st^{s'}=t^{s+s'}$. In this way, both $K[\![S]\!]$ and $K[S]$ are rings. Moreover, $K[\![S]\!]$ is a local ring whose maximal ideal is $m=(t^{n_1},\dots,t^{n_p})$, with $\{n_1,\dots,n_p\}$ the minimal system of generators of $S$ (this is why $p$ is called the embedding dimension of $S$). Some properties of $K[\![S]\!]$ and of $K[S]$ can be determined from properties of $S$. This study caused some concepts in numerical semigroups to be named after their already existing counterpart in ring theory.

The integral closure of $K[\![S]\!]$ is $K[\![t]\!]$, and if $g$ is the Frobenius number of $S$, then $t^{g+1}K[\![t]\!]\subseteq K[\![S]\!]$. This is why sometimes the Frobenius number plus one is called the conductor of $S$.

We can extend the semigroup morphism $\varphi$ described in the preceding section as follows:
\begin{equation*} 
    \psi\colon K[x_1,\dots,x_p] \to K[S],\ \psi(x_i)=t^{n_i}\ (i\in\{1,\dots,p\}
\end{equation*} 
The kernel of the ring morphism $\psi$ is known as the defining ideal of $S$.

In order to simplify the notation, we write $X^a=x_1^{a_1}\cdots x_p^{a_p}$ for $a=(a_1,\dots,a_p)\in \mathbb{N}^p$.

Herzog proved that $(a,b)\in \operatorname{Ker}(\varphi)$ if and only if $X^a-X^b\in \operatorname{Ker}(\psi)$. Moreover, if $\rho$ is a minimal presentation of $S$, then the set $\{X^a-X^b :  (a,b)\in\rho\}$ is a minimal system of generators of $\operatorname{Ker}(\psi)$.

On $K[\![S]\!]$ one can define the map $v\colon K[\![S]\!]\to S$, $v(\sum_{s\in S}a_st^s)$ to be least element in $S$ such that $a_s\not=0$. This defines a valuation on $K[\![S]\!]$. Several authors have exploited this map. If $I$ is a fractional ideal of $K[\![S]\!]$, then $v(I)$ is a relative ideal of $S$, that is, a subset of $\mathbb{Z}$ (the quotient group of $S$) such that $I+S\subseteq I$ and $I+s\subseteq S$ for some $s\in S$. If $I$ and $J$ are two fractional ideals with $J\subseteq I$, then the length of $I/J$ equals the cardinality of the set $v(I)\setminus v(J)$. In particular $I=J$ if and only if $v(I)=v(J)$.
