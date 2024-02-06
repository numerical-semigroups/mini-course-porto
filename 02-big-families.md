---
title: Big families of numerical semigroups
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

There are several families that have been of interest in the literature due to
their "extreme" properties, and for their applications in ring theory.

## Symmetric and pseudo-symmetric numerical semigroups

A symmetric numerical semigroup is a numerical semigroup without holes. Or in other words, a numerical semigroup $S$ with Frobenius number $g$ is symmetric if for every integer $x$,  $x\not \in S$, implies $g-x\in S$. Fröberg, Gottlieb and Häggkvist proved that symmetric numerical semigroups are those numerical semigroups with odd Frobenius number with the least possible number of gaps, and that this last condition is equivalent to say that they are maximal (with respect to set inclusion) in the set of numerical semigroups with the same Frobenius number. One sees in these conditions, that indeed, symmetric numerical semigroups verify some extreme properties. There are still some other characterizations. For instance, it can be shown that $S$ is symmetric if and only if the cardinality of $\operatorname{Maximals}_{\leq_S}(\operatorname{Ap}(S,n))$ is one (with $n$ any, or all, nonzero element of $S$). Recall that in particular this means that symmetric numerical semigroups are those numerical semigroups with Cohen-Macaulay type one. Kunz proved that $K[\![S]\!]$ is Gorenstein (Cohen-Macaulay ring with type equal to one) if and only if $S$ is symmetric. Thus, when looking for Gorenstein rings, one can look in the big bag of symmetric numerical semigroups, where, as Rosales showed, you can choose with given embedding dimension and multiplicity.

One might wonder if we can impose analogous restrictions to a numerical semigroup with even Frobenius number. If $g$ is the Frobenius number of $S$ and $g$ is even, then $\frac{g}2$ cannot be in $S$, and $g-\frac{g}2$ yields $\frac{g}2$. Thus the condition could be: if $x$ is an integer not in $S$ and $x\not=\frac{g}2$, then $g-x\in S$. A numerical semigroup fulfilling this condition is called pseudo-symmetric. The (Cohen-Macaulay) type of a pseudo-symmetric numerical semigroup is two (the pseudo-Frobenius numbers are $\frac{g}2$ and $g$; not every numerical semigroup with type two is pseudo-symme\-tric). These semigroups still share some nice properties with symmetric numerical semigroups: they are maximal among those numerical semigroups with the same Frobenius number, and are numerical semigroups with the least possible number of gaps.
Observe that from the point of view of fundamental gaps, both concepts can be
unified by saying that $S$ is symmetric or pseudo-symmetric if and only if the
set of fundamental gaps has a maximum with respect to $\leq_S$ (observe that
$\frac{g}2$ cannot be a fundamental gap, for $g$ the Frobenius number of $S$).
This, actually, has to do with the way we described to produce the set of all
over-semigroups of a numerical semigroup, since these semigroups are maximal
with respect to set inclusion in the set of all numerical semigroups with
Frobenius number $g$.

## Irreducible numerical semigroups

There is still another idea that unifies both families of numerical semigroups in one. A numerical semigroup is irreducible if it cannot be expressed as the intersection of two numerical semigroups containing it properly. It turns out that irreducible equals maximality with respect to set inclusion in the set of all numerical semigroups with given Frobenius number. Thus, a numerical semigroup is irreducible if and only if it is symmetric (and thus has odd Frobenius number) or pseudo-symmetric (with even Frobenius number).

Every numerical semigroup can be expressed as the intersection of finitely many irreducible numerical semigroups. Branco and Rosales did a nice work characterizing these factorizations, and studying which semigroups could be expressed in terms of just symmetric or pseudo-symmetric numerical semigroups. We know how to produce minimal decompositions, but still do not have any idea of the number of numerical semigroups involved in such a decomposition, in contrast of which is known for ideals of polynomial rings.

## Complete intersections 

A numerical semigroup is a complete intersection if the cardinality of any of its minimal presentations equals its embedding dimension minus one (recall that the embedding dimension is the cardinality of the minimal system of generators of the numerical semigroup). This, in terms of numerical semigroups, means that the semigroup can be described with the least possible number relations. Hence again we have an "extreme" condition characterizing a family of numerical semigroups. It turns out that complete intersections are always symmetric. Thus many authors while looking for examples of Gorenstein rings chose semigroup rings over a complete intersection numerical semigroup (which are as rings a complete intersection, as expected). Delorme proved that a numerical semigroup is a complete intersection if it is the gluing of two complete intersection numerical semigroups, where gluing roughly speaking means that the presentation of the resulting semigroup is obtained by the presentations of each of the semigroups glued plus one relation connecting the generators of the first semigroup with the generators of the second. Numerical semigroups generated by two elements are the easiest example of complete intersections. If we are able to glue a numerical semigroup generated by two elements with a submonoid of $\mathbb{N}$ generated by one element (and thus with no relators), the resulting semigroup is again a complete intersection. We can repeat this procedure and obtain complete intersections with more than three generators. The semigroups obtained are called telescopic, and their presentations have, from the way they are constructed, a stair shape. Since they are relatively easy to construct, these semigroups have been extensively used in the literature.

## Maximal embedding dimension numerical semigroups

The multiplicity (least element) of a numerical semigroup is an upper bound for the embedding dimension (number of minimal generators). When this bound is reached, we obtain a maximal embedding dimension numerical semigroup. These semigroups not only fulfill this maximal condition, but also they are those with the maximum possible number of relators. This was proved by Sally and the equivalence by Rosales. Observe also that for these semigroups, every nonzero element of the Apéry set of the numerical semigroup with respect to its multiplicity is a minimal generator (the converse is always true, every minimal generator other than the multiplicity is in any Apéry set).

If $S$ is a numerical semigroup, $m$ is its multiplicity, and as usual we write $\operatorname{Ap}(S,m)=\{0,w_1,\ldots,w_{m-1}\}$, then $\langle m,m+w_1,\ldots,m+w_{m-1}\rangle$ is a maximal embedding dimension numerical semigroup. This exhibits the abundance of semigroups of this kind. Observe that $m+w_i>2m$ for all $i$. If we take a maximal embedding dimension numerical semigroup $\langle m,x_1,\ldots,x_{m-1}\rangle$ such that $x_i>2m$ for all $i$, then $S=\langle m,x_1-m,\ldots,x_{m-1}-m\rangle$ is a numerical semigroup with multiplicity $m$ and $\operatorname{Ap}(S,m)=\{0,x_1-m,\ldots,x_{m-1}-m\}$. Thus there is a one to one correspondence between the set of numerical semigroups with multiplicity $m$ and the set of maximal embedding dimension with multiplicity $m$ verifying that every generator other than the multiplicity is greater than twice the multiplicity.

There are several ways to characterize the maximal embedding dimension property, but we will focus on the following one, which will allow us to introduce some restrictions and will be the inspiration for what comes later in this session. A numerical semigroup $S$ is of maximal embedding dimension if and only if for every $x$ and $y$ nonzero elements of $S$, $x+y-m\in S$, where $m$ is the multiplicity of $S$. From this it easily follows that the intersection of two maximal embedding dimension numerical semigroups sharing the same multiplicity is again a maximal embedding dimension with the same multiplicity. Moreover if $S$ is a maximal embedding dimension numerical semigroup with multiplicity $m$ and Frobenius number $g$, then so is $S\cup\{g\}$.

Note that in the condition $x+y-m\in S$, we are choosing $x,y\in S\setminus\{0\}$, or in other words, $x,y\in S$ with $x,y\geq m$. Thus we can slightly modify this condition by: for every $x$, $y$ and $z$ in $S$, with $x,y\geq z$, we have that $x+y-z\in S$. A numerical semigroup fulfilling this condition is (trivially) a maximal embedding dimension numerical semigroup, but not every maximal embedding dimension numerical semigroup has this property. This condition is known as the Arf property. If two numerical semigroups have the Arf property, so does the intersection. This class is also closed under adjoin of the Frobenius number (observe that no restriction on the multiplicity is required here).

## Families closed under intersection and adjoin of the Frobenius number

As we have seen above some families of numerical semigroups $\mathcal{F}$ fulfill that

- (C1) if $S_1,S_2\in \mathcal{F}$, then $S_1\cap S_2\in \mathcal{F}$,
- (C2) if $S\in \mathcal{F}$ and $g$ is the Frobenius number of $S$, then $S\cup\{g\}\in \mathcal{F}$.

We can think on the numerical semigroup $S$ generated in $\mathcal{F}$ by a subset $A$ of $\mathbb{N}$ with greatest common divisor equal to one. This semigroup can be defined as the intersection of all $T\in\mathcal{F}$ such that $A\subseteq T$. We then say that $A$ is an $\mathcal{F}$-system of generators of $S$, or that $S$ is the $\mathcal{F}$-closure of $S$. Of course, we say that $A$ is minimal if no proper subset of $A$ $\mathcal{F}$-generates $S$. We observed that for the families of maximal embedding dimension numerical semigroups with fixed multiplicity, numerical semigroups having the Arf property (and also those having the saturated property, a generalization of the Arf property) and  system proportionally modular numerical semigroups (of which we will talk in our next lecture), minimal $\mathcal{F}$-systems of generators where unique. All these families had in common that (C1) and (C2) hold for them. Moreover, an element is in a minimal $\mathcal{F}$-system of generators of $S$ if and only if $S\setminus \{m\}$ is again in $\mathcal{F}$, just as happens with "classical" minimal generators. This enabled us to obtain recurrently the tree of all numerical semigroups in these families.

Rosales proved that these two conditions suffice to show that $\mathcal{F}$-minimal systems of generators are unique.
