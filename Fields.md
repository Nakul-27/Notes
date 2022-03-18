---
aliases: [""] 
tags: [AbstractAlgebra, GroupTheory] 
dateCreated: 2022-03-05 18:56:08
---
# Fields
A set together with two laws of composition (Definition 3.2.2 in Artin):
$$
\begin{align*}
	1. \text{ } &F \times F \stackrel{+}{\rightarrow} F\\\\
	2. \text{ } &F \times F \stackrel{\times}{\rightarrow} F
\end{align*}
$$
**Note:** That these operations are called addition and multiplication denoted as $a,b \rightsquigarrow a + b$ and $a,b \rightsquigarrow ab$ respectively which satisfy the following 3 axioms:
1. Addition makes $F$ into an **abelian Group** $F^+$; its identity element is denoted by $0$. 
2. Multiplication is commutative, and it makes the set of nonzero elements of $F$ into an abelian group $F^\times$; its identity is denoted by $1$. 
3. *Distributive law*; For all $a, b, \text{ and }c$ in $F$, $a(b + c) = ab + ac$. (Relates (1) and (2))

## Lectures

## Readings
[[Emil Artin|Artin]] Section 3.2 #textbook 
[[Michael Artin|Artin]] Section 15
[[JBF]] Sections 21

# Lemmas
### Lemma 3.2.3 - Artin
Let $F$ be a field.
1. The elements $0$ and $1$ of $F$ are distinct.
2. For all $a$ in $F$, $a0 = 0$ and $0a = 0$.
3. Multiplication in $F$ is associative, and $1$ is an identity element.

# Theorems
### Theorem 3.25 - Artin
Let $p$ be a prime integer. Every nonzero congruence class modulo $p$ has a multiplicative inverse, and therefore $\mathbb{F}_p = \{\overline{0}, \overline{1}, \ldots, \overline{p - 1}\} = \mathbb{Z}/p\mathbb{Z}$ is a field of order $p$. 

### Theorem 21.6 - JBF

Let $F$ be a field of quotients of $D$ and let $L$ be any field containing $D$. Then there exists a map $\psi: F \rightarrow L$ that gives an isomorphism of $F$ with a subfield of $L$ such that $\psi(a) = a$ for $a \in D$.

![[Pasted image 20220315215101.png]]
