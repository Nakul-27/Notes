---
aliases: [""] 
tags: [AbstractAlgebra, GroupTheory] 
dateCreated: 2022-03-05 18:56:50
---
# Rings
**Rings:** Algebraic Structures that are closed under addition, subtraction, and multiplication, but not under division. 

![[Pasted image 20220315204410.png]]

## Lectures

## Readings
[[Michael Artin|Artin]] Chapter 11 #textbook 
[[JBF]] Sections 18 - 20
## Corollaries

### Corollary 11.2.11 - Artin

Let $g(x)$ be a polynomial in $R[x]$, and let $\alpha$ be an element of $R$. The remainder of division of $g(x)$ by $x- \alpha$ is $g(\alpha)$. Thus $x - \alpha$ divides $g$ in $R[x]$ if and only if $g(\alpha) = 0$. 

### Corollary 20.2 - JBF

If $a \in \mathbb{Z}$, then $a^p \equiv a$ mod $p$ for any prime $p$.

## Lemmas

## Definitions

### Defintion 11.1.3 - Artin
A ring $R$ is a set with two laws of composition, $+$, and $\times$, called addition and multiplication, that satisfy these axioms:
1. With the law of composition $+$, $R$ is an abelian group that we denote by $R^+$; its identity is denoted by $0$. 
2. Multiplication is commutative and associative, and has an identity denoted by $1$. 
3. *Distributive law*: For all $a,b,c \in R$, $(a + b)c = ac + bc$. 

**Note:** A *subring* of a ring is a subset that is closed under the operations of addition, subtraction, and multiplication that contains the element $1$. 

**Note:** A *non-commutative-ring* is a ring that doesn't satisfy axiom (3). The set of all real $n \times n$ matrices is one such example. Commutative rings are by definition Abelian.

## Theorems

### Theorem 20.1 - JBF ([[Pierre de Fermat|Fermat]]'s Little Theorem)

If $a \in \mathbb{Z}$ and $p$ is a prime not dividing $a$, then $a^{p-1} \equiv 1$ mod $p$ for $a \not\equiv 0$ mod $p$.

### Theorem 20.6 - JBF

3
The set $G_n$ of nonzero element of $\mathbb{Z}_n$ that are not $0$ divisors forms a group under multiplication modulo $n$.

Define $\varphi(n)$ as the number of positive integers that are less than or equal to $n$ and relatively prime to $n$ with $\varphi(1) = 1$. Note that this is known as the [[Leonhard Euler|Euler]] phi-function.

### Theorem 20.8- JBF ([[Leonhard Euler|Euler]]'s Theorem)

If $a$ is an integer relatively prime to $n$, then $a^{\varphi(n)} \equiv 1$ mod $n$. 

### Theorem 22.1 - JBF

The set $R[x]$ of all polynomials is an indeterminate $x$ with coefficients in a ring $R$ is a ring under polynomial addition and multiplication. If $R$ is commutative, then so is $R[x]$, and if $R$ has unity $1 \not= 0$, then $1$ is also unity of $R[x]$.

### Theorem 22.4 - JBF

Let $F$ be a subfield of a [[Fields]] $E$. let $\alpha$ be any element of $E$, and let $x$ be an intermediate. The map $\phi_\alpha : F[x] \rightarrow E$ defined by:
$$
	\phi_\alpha (a_0 + a_1x + \ldots + a_nx^n) = a_0 + a_1\alpha + \ldots + a_n \alpha^n
$$
for $(a_0 + a_1x + \ldots + a_nx^n) \in F[x]$ is a homomorphism of $F[x]$ into $E$. Also $\phi_\alpha(x) = \alpha$ and $\phi_\alpha$ maps $F$ isomorphically by the identity map; that is $\phi_\alpha(a) = a$ for $a \in F$. The homomorphism $\phi_\alpha$ is the **evaluation at** $\alpha$.

![[Pasted image 20220318104724.png]]

## Polynomial Ring

A polynomial with coefficients in a ring $R$ is a (finite) linear combination of powers of the variable:
$$
	f(x) = a_nx^n + a_{n-1}x^{n-1} + \ldots + a_1x + a_0,
$$
with $a_i$ in $R$. The set of these polynomials forms a ring. This means that $\mathbb{Z}[x]$ denotes the set of polynomials with integer coefficients or *the set of integer polynomials.*

### Monomials
The monomials $x^i$ are considered independents. So if given
$$
	f(x) = a_nx^n + a_{n-1}x^{n-1} + \ldots + a_1x + a_0,
$$
and 
$$
	g(x) = b_mx^m + b_{m-1}x^{m-1} + \ldots + b_1x + b_0,
$$
which are both in $R$, then $f(x)$ and $g(x)$ are equal if and only if $a_i = b_i$ for all $i = 0, 1, 2, \ldots$ .

A *monic* polynomial is one whose leading coefficient is $1$. 

### Degree

The degree of a non-zero polynomial which may be denoted as $deg \text{ } f$, is the largest integer $n$ such that the coefficient $a_n$ of $x_n$ is not zero. 

### Addition and Products

Define addition of Polynomials as:
$$
	f(x) + g(x) = (a_0 + b_0) + (a_1 + b_1)x + \ldots = \sum_{k}(a_k + b_k)x^k,
$$
where the notation $(a_i + b_i)$ refers to addition in $R$. So vector addition can be defined as $a + b = (a_0 + b_0, a_1 + b_1, \ldots)$ 

Define products of Polynomials as:
$$
	f(x)g(x) = (a_0 + a_1x + \ldots)(b_0 + b_1x + \ldots) = \sum_{i,j} (a_ib_j)x^{i+j},
$$
where the products $a_ib_j$ are to be evaluated in the ring $R$. This can be rewritten as
$$
	f(x)g(x) = p_0 + p_1x + p_2x^2 + \ldots
$$
with                                                    $p_k = \sum_{i + j = k}a_ib_j,$

$$
	p_0 = a_0b_0, \text{ } p_1 = a_0b_1 + a_1b_0, \text{ } p_2 = a_0b_2 + a_1b_1 + a_2b_0, \ldots
$$
Each $p_k$ is evaluated using the laws of composition in the ring. However, when making computations, it may be desirable to defer the collection of terms temporarily.

**The ring $R$ becomes a subring of $R[x]$ when the elements of $R$ are identified with the constant polynomials.**

## Division with Remainder

Let $R$ be a ring, let $f$ be a monic polynomial and let $g$ be any polynomial, both with coefficients in $R$. There are uniquely determined polynomials $q$ and $r$ in $R[x]$ such that 
$$
	g(x) = f(x)q(x) + r(x),
$$
and such that the remainder $r$, if it is not zero, has degree less than the degree of $f$. Moreover, $f$ divides $g$ in $R[x]$ if and only if the remainder $r$ is zero. 

## Zero Ring

A ring, $R$, in which the elements $1$ and $0$ are equal.

## Homomorphisms and Ideals

### Ring Homomorphism

A ring homomorphism $\varphi: R \rightarrow R'$ is a map from one ring to another which is compatible with the laws of composition and which carries the unit element $1$ of $R$ to the unit element $1$ in $R'$. Satisfies the following:
$$
\begin{align*}
1. \text{ } & \varphi(a + b) = \varphi(a) + \varphi(b)\\
2. \text{ } & \varphi(ab) = \varphi(a)\varphi(b)\\
3. \text{ } & \varphi(1) = 1
\end{align*}
$$
The map

$$
\varphi: \mathbb{Z} \rightarrow \mathbb{F}_p
$$
that sends an integer to its congruence class modulo $p$ is a ring homomorphism.

### Ring Isomorphism

$R \approx R'$ indicates that two rings are isomorphic.

**The most important ring homomorphisms are obtained by evaluating polynomials. Evaluation of real polynomials at a real number $a$ defines $\mathbb{R}[x] \rightarrow R$, that sends $p(x) \rightsquigarrow p(a)$.**
- Similarly, one can also evaluate real polynomials at a complex number such as $i$, which will obtain the homomorphism $\mathbb{R}[x] \rightarrow \mathbb{C}$ that sends $p(x) \rightsquigarrow p(i)$. 

### Superposition Principle - Prop 11.3.4 Artin

Let $\varphi: R \rightarrow R'$ be a ring homomorphism, and let $R[x]$ be the ring of polynomials with coefficients in $R$. 
1. Let $\alpha$ be an element of $R'$. There is a unique homomorphism $\Phi: R[x] \rightarrow R'$ that agrees with the map $\varphi$ on constant polynomials and that sends $x \rightsquigarrow \alpha$. 
2. More generally, given elements $\alpha_1, \ldots, \alpha_n$ of $R'$, there is a unique homomorphism $\Phi: R[x_1, \ldots, x_n] \rightarrow R'$, from the polynomial ring in $n$ variables to $R'$, that agrees with $\varphi$ on constant polynomials and that sends $x_v \rightsquigarrow \alpha_v$ for $v = 1, \ldots, n$. 

### Ideals

An ideal (ideal element) $I$ of a ring $R$ is a nonempty subset of $R$ with the following properties:
1. $I$ is closed under addition
2. if $s$ is in $I$, and $r$ is in $R$, then $rs$ is in $I$.
**Note:** The kernel of a ring homomorphism is an ideal. 

#### Kernel

Let $\varphi: R \rightarrow R'$ be a ring homomorphism. Define the Kernel as the set of elements that map to $0$:

$$
I = ker \varphi = \{s \in R|\varphi(s) = 0\}.
$$