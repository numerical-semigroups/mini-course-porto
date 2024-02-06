---
title: Numerical semigroups and Diophantine inequalities
authors:
  - name: Pedro A. García Sánchez
    affiliations:
      - Universidad de Granada
exports:
  - format: pdf
    template: curvenote
    article_type: paper
    output: exports/matrices.pdf
---

In our first lecture, the connection between numerical semigroups and Diophantine equalities was made explicit. In this last lecture we will show how the set of all numerical semigroups with fixed multiplicity can be described in terms of a finite system of Diophantine inequalities. We will also give some families of numerical semigroups that can be defined as the set of solutions of a Diophantine inequality.

## The set of all numerical semigroups with fixed multiplicity is a monoid

We say that a set $X\subseteq \N$ is a complete system modulo a positive integer $m$ if the cardinality of $X$ is $m$ and for every $i\in\{1,\ldots,m\}$ there exists $x_i\in X$ congruent with $i$ modulo $m$. This property might sound familiar to the reader, since Apéry sets with respect to an element in a numerical semigroup fulfilled this condition. Not every complete system modulo $m$ is the Apéry set of a numerical semigroup containing $m$, there is still another restrictions required: first that $x_0=0$, and second that $x_i+x_j=x_{(i+j)\mod m}+k m$ for some nonnegative integer $k$. Observe also that if $X$ is the Apéry set of a numerical semigroup $S$ in $m$, then $X\cup\{m\}$ generates $S$ and completely determines it (just recall the nice properties of Apéry sets). If one wants to use Apéry sets to describe a numerical semigroup, the cheapest choice is to take the Apéry set with respect to the multiplicity, since this has the least possible number of elements.

Let $S$ be a numerical semigroup and $m$ be its multiplicity. If $\operatorname{Ap}(S,m)=\{w_0=0,w_1,\ldots,w_{m-1}\}$ with $w_i$ congruent to $i$ modulo $m$, then $w_i= k_i m +i$ for some nonnegative integer $k_i$. Since $m$ is the multiplicity and $w_i\in S$, if $i\not=0$, then $w_i\geq m$ and thus $k_i\geq 1$. The condition $w_i+w_j=w_{(i+j)\mod m}+km$ translates to $(k_i+k_j)m+i+j=k_{(i+j)\mod m}m+(i+j)\mod m +km$. As $i+j=\lfloor \frac{i+j}m\rfloor m+ (i+j)\mod m$,  we obtain that  $(k_1,\ldots,k_{m-1})$ ($k_0=0=w_0$ gives no information) is a nonnegative integer solution to the system of inequalities

\begin{equation}\label{london}
\left\{
\begin{array}{rll}
x_i & \geq 1, & 1\leq i\leq m-1, \\
x_i+x_j +\lfloor \frac{i+j}m\rfloor & \geq x_{(i+j)\mod m}, & 1\leq i\leq
j\leq m-1, i+j\not=m.
\end{array} \right.
\end{equation}

Moreover, if $(k_1,\ldots,k_{m-1})$ is a nonnegative integer solution to [](#london), then 

\begin{equation*}
S=\langle m,k_1m+1,k_2m+2,\ldots,k_{m-1}m+m-1\rangle
\end{equation*} 

is a numerical semigroup with multiplicity $m$ and $\operatorname{Ap}(S,m)=\{0,k_1m+1,k_2m+2,\ldots,k_{m-1}m+m-1\}$. Let ${\mathcal T}(m)$ be the set of elements of $\N^{m-1}$ that are solutions of [](#london). Then ${\mathcal T}(m)$ is the ideal of a finitely generated commutative monoid (the monoid of solutions of the associated homogeneous system of inequalities, which belongs to a class of affine semigroups that has been widely studied in the literature). Thus this set can be described by a finite set of elements in $\N^{m-1}$, and it is bijective with the set of all numerical semigroups with multiplicity $m$.

If one changes the inequalities $x_i+x_j +\lfloor \frac{i+j}m\rfloor  \geq x_{(i+j)\mod m}$ in [](#london) with $x_i+x_j +\lfloor \frac{i+j}m\rfloor > x_{(i+j)\mod m}$ (or equivalently with $x_i+x_j +\lfloor \frac{i+j}m\rfloor \geq x_{(i+j)\mod m}+1$), then the set of nonnegative integer solutions to this new system corresponds to the set of maximal embedding dimension numerical semigroups with multiplicity $m$. This set of solutions is a submonoid of $\N^{m-1}$, and using the correspondence described in our last lecture between numerical semigroups with multiplicity $m$ and maximal embedding dimension numerical semigroups with multiplicity $m$ and the rest of minimal generators greater than $2m$, one obtains that the set of numerical semigroups with fixed multiplicity is a monoid (isomorphic to the one obtained by replacing $x_i\geq 1$ with $x_i\geq 2$).

## Modular Diophantine numerical semigroups

Fixed $m$ a nonzero element in a numerical semigroup, recall that a non\-ne\-gative integer $x$ belongs to $S$ if and only if $w_{x\mod m}\leq x$, where $w_i$ stands for the least element in $S$ congruent with $i$ modulo $m$ (these are precisely the elements in $\operatorname{Ap}(S,m)$). If we define $f_S:\N \to \mathbb{Q}$ (needless to say that we use $\mathbb{Q}$ to denote the set of rational numbers) as $f_S(x)=w_{x\mod m}$, then, in view of the properties of the Apéry set studied in the preceding section, $f_S(x+y)\leq f_S(x)+f_S(y)$. Observe also that $f_S(x+m)=f_S(x)$, that is, $f_S$ is subadditive, $f_S(0)=0$ and it is periodic with period $m$. Moreover,
\begin{equation*}
    S=\{x\in \N : f_S(x)\leq x\}.
\end{equation*}
The converse is also true, every subadditive function $f$ such that $f(0)=0$ and $f(x+m)=f(x)$ defines a numerical semigroup
\begin{equation*} 
    S_f=\{x\in \N : f(x)\leq x\}.
\end{equation*}
Let $a$ and $b$ be positive integers, and set $f(x)=ax\mod b$. Then $f$ is subadditive, $f(0)=0$ and $f(x+b)=f(x)$. Thus
\begin{equation*}
    \operatorname{S}(a,b)=\{ x\in \N : ax\mod b\leq x\}
\end{equation*}
is a numerical semigroup. We say that a numerical semigroup $S$ is modular if there exist $a$ and $b$ such that $S=\operatorname{S}(a,b)$. This was the beginning of a research that yielded Urbano-Blanco's thesis and in which M. Delgado was also engaged (together with our team in Granada).

Even though the membership problem for these semigroups is trivial, surprisingly we know relatively few things about these semigroups. We still do not know a formula for the Frobenius number in terms of $a$ and $b$, neither for the multiplicity. However the cardinality of the set of gaps of $\operatorname{S}(a,b)$ is
\begin{equation*}
    \frac{b+1-\gcd\{a,b\}-gcd\{a-1,b\}}2.
\end{equation*}
This formula was not obtained using Selmer's formula (presented the first day), since we do not have a nice way to describe the set of elements in the Apéry sets of $\operatorname{S}(a,b)$. Recall that symmetric and pseudo-symmetric numerical semigroups were numerical semigroups with the least possible number of gaps with odd and even Frobenius number, respectively. Thus if $S$ is symmetric (respectively pseudo-symmetric) with Frobenius number $g$, then the cardinality of the set of gaps of $S$ is $\frac{g+1}2$ (respectively $\frac{g+2}2$). In this way it is easy to derive when a modular numerical semigroup is symmetric or pseudo-symmetric.

We were able to describe, for some subfamilies of modular numerical semigroups, some of the invariants mentioned above. We found also an algorithm procedure to recognize modular numerical semigroups, which has been recently improved by Urbano-Blanco and Rosales, giving all possible pairs $a$ and $b$ for which a numerical semigroup $S=\operatorname{S}(a,b)$. These improvements were achieve by using Bézout sequences, which are the topic of our next section.

## Proportionally modular Diophantine numerical semigroups

If we choose now $f(x)=\frac{1}c (ax\mod b)$, with $a$, $b$ and $c$ positive integers, then this map is also subadditive, $f(0)=0$ and $f(x+b)=f(x)$ for all $x\in \N$. Thus
\begin{equation*}
\operatorname{S}(a,b,c)=\{ x\in \N : ax\mod b\leq cx\}
\end{equation*}
is a numerical semigroup. These semigroups are known as proportionally modular numerical semigroup, and clearly, every modular numerical semigroup belongs to this class. The point is that we do not have in general, as we had for modular numerical semigroups, a formula of the number of gaps of $\operatorname{S}(a,b,c)$. However while generalizing from modular to proportionally modular, we learned a lot more than we knew about modular numerical semigroups, due mainly to the tools we developed in this more general setting. We explain briefly some of them here.

Assume that $I$ is a non-empty interval of $\mathbb{Q}^+$. The submonoid of $\mathbb{Q}^+$ generated by $I$ is $\bigcup_{k\in \N} kI$. If we cut this monoid with $\N$, we obtain a numerical semigroup, which amazingly is always a proportionally modular numerical semigroup. We will denote this numerical semigroup by $\operatorname{S}(I)$. Moreover, every proportionally numerical semigroup can be obtained in this way:
\begin{equation*} 
    \operatorname{S}(a,b,c)=\operatorname{s}\Big(\big[\frac{b}a,\frac{b}{a-c}\big]\Big)
\end{equation*}
(since we are performing computations modulo $b$, we can assume that $a<b$, and if $c\geq a$, then trivially $\operatorname{S}(a,b,c)=\N$; thus we assume that $c<a<b$). This in particular means that for every nonnegative integer $x$, we have that $x\in \operatorname{S}(a,b,c)$ if and only if there exists $k\in \N\setminus\{0\}$ such that $\frac{b}a\leq \frac{x}k\leq \frac{b}{a-c}$ (from the restrictions assumed for $a$, $b$ and $c$, this implies that $k\in\{1,\ldots,x-1\}$). This allows us to decide if a numerical semigroup is proportionally modular or not, since we only have to find $\alpha$ and $\beta$ in $\mathbb{Q}$ such that for every minimal generator $n$ of the semigroup there is a $k\in\{1,\ldots,x-1\}$ for which $\alpha\leq \frac{n}k\leq \beta$, and such that for every fundamental gap $h$ there is not such $k$.

If $a$, $b$, $c$ and $d$ are positive integers such that $\frac{a}{c}<\frac{b}d$ and $bc-ad=1$, then it can be shown that $\operatorname{S}([\frac{a}c,\frac{b}d])=\langle a,b\rangle$. Thus this enables us to compute a system of generators of $\operatorname{S}([\frac{a}c,\frac{b}d])$, when $bc-ad=1$. But, what happens if $ad-bc>1$? How can we obtain a generating system for $\operatorname{S}([\frac{a}c,\frac{b}d])$? If we were able to solve this, for any $a,b,c\in \N$, we would be able to determine those integers that are solution to $ax \mod b\leq cx$, or in other words, find a system of generators of $\operatorname{S}(a,b,c)$.

Thus let us go back once more to the problem of finding a system of generators of $\operatorname{S}([\frac{a}c,\frac{b}d])$, and assume that there are $a_1,\ldots,a_n$ and $b_1,\ldots,b_1$ positive integers such that

- $\frac{a_1}{b_1}<\cdots<\frac{a_n}{b_n}$,
- for all $i\in\{1,\ldots,n-1\}$, $a_{i+1}b_i-a_ib_{i+1}=1$,
- $\frac{a_1}{b_1}=\frac{a}c$ and $\frac{a_n}{b_n}=\frac{b}d$.

Then $\frac{a}c<\frac{x}k <\frac{b}d$ if and only if for some $i\in\{1,\ldots,n-1\}$, $\frac{a_i}{b_i}<\frac{x}k <\frac{a_{i+1}}{b_{i+1}}$, or equivalently, $x\in \langle a_i,a_{i+1}\rangle$. Thus if such a sequence exists, $\operatorname{S}([\frac{a}c,\frac{b}d])=\langle a_1,\ldots,a_n\rangle$ (moreover, $\operatorname{S}([\frac{a}c,\frac{b}d])=\langle a_1,a_2\rangle \cup \cdots \cup\langle a_{n-1},a_n\rangle$).

We say that the sequence $\frac{a_1}{b_1}<\cdots <\frac{a_n}{b_n}$ is a Bézout sequence joining $\frac{a}c$ and $\frac{b}d$. Bézout sequences connecting a rational number with another larger rational number always exist and are easy to compute. Their properties have shed some light in the world of proportionally modular numerical semigroups. For instance, we know that the numerators of a Bézout sequence form a convex sequence, whence the first two minimal generators of a proportionally modular numerical semigroup are always adjacent in the sequence. This in particular means that they are coprime. Hence $\langle 4,6,7\rangle$ is not a proportionally modular numerical semigroup.

## Toms' result 

We say that a numerical semigroup $S$ is system proportionally modular if it is the intersection of finitely many proportionally modular numerical semigroups. That is, $S$ is the set of integer solutions to a system of equations of the form:
\begin{equation*}
\left\{
\begin{array}{c}
a_1 x \mod b_1 \leq c_1 x,\\
a_2 x \mod b_2 \leq c_2 x,\\
\vdots\\
a_k x \mod b_k\leq c_k x,
\end{array}
\right.
\end{equation*}
with $a_i,b_i,c_i$ positive integers. Trivially, system proportionally modular numerical semigroups are closed under intersections, and it can be shown that they are closed also under the operation of adjoining the Frobenius number. Thus, as seen in the last lecture, it makes sense to talk about minimal systems of generators for numerical semigroups in this family, and one can recurrently construct the set of all system proportionally numerical semigroups and arrange it in a tree. We already knew that some irreducible numerical semigroups were not proportionally modular, and thus not every numerical semigroup is system proportionally modular.

Urbano-Blanco and Rosales proved that every proportionally modular numerical semigroup is of the form $\frac{\langle m,n\rangle}d$, where in general for a numerical semigroup $S$ and a positive integer $d$,

\begin{equation*} 
    \frac{S}d=\{ x\in \N : dx\in S\},
\end{equation*}

which is also a numerical semigroup. Unfortunately even if we have a formula for the Frobenius number of $S$ (as we have for $\langle n_1,n_2\rangle$), we do not know how is the Frobenius number of $\frac{S}d$. The same stands for the minimal generators and other invariants of the semigroup.

It follows that every system proportionally numerical semigroup  can be expressed as $\frac{\langle m_1,n_1\rangle}{d_1}\cap \cdots \cap \frac{\langle m_l,n_l\rangle}{d_l}$. We were able to show that modifying conveniently $m_i$ and $n_i$, we could choose $d_1=\cdots=d_l$, and so that $m_i,n_i,d_i$ are pairwise coprime. We were looking for this since recently Toms proved that for numerical semigroups $S$ of this form, there is always a $C^*$-algebra for which its $K_0$-ordered group is isomorphic to $(\Z,S)$.

We already know that not every numerical semigroup is system proportionally modular, but the question of determining a $C^*$-algebra fulfilling the above condition for this semigroup still remains open.
