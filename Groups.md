---
aliases: [""] 
tags: [Math, AbstractAlgebra, GroupTheory] 
dateCreated: 2022-02-23 08:02:00
---
# Groups
**A First Course in Abstract Algebra** #textbook
##  Lectures
### Video Playlists
[Abstract Algebra](https://youtube.com/playlist?list=PLelIK3uylPMGzHBuR3hLMHrYfMqWWsmx5)
[Visual Group Theory](https://youtube.com/playlist?list=PLwV-9DG53NDxU337smpTwm6sef4x-SCLv)

Groups are [[Sets]] but with specific Rules

## Rules of a Group
1.  A set with a product structure, $a, b \in G$ then $a \cdot b \in G$ 
2. Associativity
3. Has an identity element $e$. $a \cdot e = e \cdot a = a$.
4. Inverse $g^{-1}$. $gg^{-1} = g^{-1}g = e$.

Note that indistinguishable actions are the same.

**Inverse** - The opposite of an action. An action $g$ has an inverse 

## Subgroup
A Subset of a group that is 
1. Closed under multiplication
2. Contains the identity
3. Closed under inverses.

### Cyclic Subgroup
When a generator generates infinite elements a cyclic subgroup has *infinite order.* (Generator does not produce the Identity element)

Ex: 
$$
\left \langle
\begin{pmatrix}
	1 & 1 \\
	0 & 1
\end{pmatrix}
\right \rangle = 
\left \{
\begin{pmatrix}
	1 & 1 \\
	0 & 1
\end{pmatrix}^n = 
\begin{pmatrix}
	1 & n \\
	0 & 1
\end{pmatrix} \hspace{0.2cm} n \in \mathbb{Z}
\right \}
$$

### Normal Subgroups
A Subgroup $H$ of a group $G$ that has the property that $gHg^{-1} = H \hspace{0.2cm} \forall \hspace{0.2cm} g \in G$. Denoted as $H \lhd G$. 
*Note that $gHg^{-1}$ is denoted as the Conjugation*
**Normal Subgroups are closed under conjugation by $G$.**

#### Example of a Group that is not Normal
Allow $G = S_3$ and $H = \langle e, \tau \rangle$.
Test via conjugation: $\tau(3) = 3$
$$
\begin{align*}
	\tau' \tau (\tau')^{-1} &= \tau' \tau \tau'(3) \\
	&=\tau' \tau (2)\\
	&=\tau'(1)\\
	&= 1
\end{align*}$$
Since $\tau' \tau (\tau')^{-1} = \tau''$ this group is not normal. This further means that $\tau H\tau^{-1} = \langle e, \tau'' \rangle$. 

## [[Abelian Groups]]

## [[Cyclic Groups]]
**FACT:** Every two cyclic groups, $G_1, G_2$ of order $n$ are isomorphic. 
- This is because there exists an isomorphism between $G_1$ and $G_2$ such that $f(X_1^k) = X_2^k$ is a well defined bijection . Specifically because $G_1$ and $G_2$ have the same order. 
- There is always a cyclic group of order $n$.
	- Take the Cyclic Subgroups $C_n = \langle \sigma_n \rangle \subset S_n$. where $|C_n| = n$.


## [[Generators]] 
Need enough generators to generate the whole group.

$G = \langle$ generators $|$ relations $\rangle$ 
$V_4 = \langle a,b | a^2 = e, b^2 = e, ab = ba \rangle$ 

Ex: Take the Rectangle
![[Pasted image 20220222213128.png]]
We can define a Group that has the following 4 actions:
1. Do nothing
2. Flip Horizontally ($h$)
3. Flip Vertically ($v$)
4. Rotate 180 degrees ($r$)

We can say that $G = \langle h,v \rangle$ . Meaning that $\langle h, v \rangle$ is a generator of the Rectangle Group

Note also that $r = hv = vh$. Meaning that $G$ is abelian.

## [[Cayley Graphs]]
Cayley Graph for Generator Example above:
![[Pasted image 20220222213700.png]]

Any group with 4 elements is a *Klein four-group*. Denoted as $V_4$.

Cayley Graph for $D_3$ (Non-Abelian):
![[Pasted image 20220222214457.png]]

### Abstract Cayley Graph
A Cayley Graph where the labels are the actions
Ex: $V_4$
![[Pasted image 20220222220816.png]]

Ex: $D_3$
![[Pasted image 20220222220956.png]]
or 
![[Pasted image 20220222221003.png]]

### Cayley's Theorem
**Every Group can be represented as a collection of symmetries.**

## [[Multiplication Tables]]
Shows how every pair of group actions combine.
Ex: ![[Pasted image 20220222221733.png]]
## [[Isomorphism]]
When two groups have the same structure but "have different labelling". *Same Multiplication Table*
**Preserves the Homomorphism Property**
Example: Take $G_1 = (\mathbb{R}, +) $ $G_2 = (\mathbb{R}_{> 0}, \times)$ 
Define $f: G_1 \rightarrow G_2$ where $f(x) = e^x$.

#### Homomorphism
Map $f: G \rightarrow G'$ such that the homomorphism property is defined: 
1. $f(x \cdot y) = f(x) \cdot f(y)$
2. $f(e) = e'$
3. $f(g^{-1}) = f(g)^{-1}$ 
***Note that $2$ and $3$ are implied.***

There always exists a *trivial homomorphism* between two groups: $f: G_1 \rightarrow G_2$ where $f(x) = e$.

##### Image
Image $= \{g' = f(g) \text{ in } G'\} \subset G$
##### Kernel
Kernel $= H = \{g: f(g) = e'\} \subset G$ 
*Always has the property that $H \lhd G$ .*
##### Center
$Z(G) = \{z \in G: zg = gz \text{ for all } g\}$
If $G$ is abelian, then $G = Z(G)$.
If $G = S_n$, then $Z(G) = \{e\}$.

##### Homomorphism Example
$f: S_n \rightarrow GL_n(\mathbb{R})$
$f(\sigma) = A_\sigma =$ permutation on matrix associated to $\sigma$.

Ex with $G = S_3$:
$\sigma$ sends $1 \rightarrow 2$, $2 \rightarrow 3$, $3 \rightarrow 1$.
Permutation Matrix: 
$$
\begin{pmatrix}
	0 & 0 & 1 \\
	1 & 0 & 0 \\
	0 & 1 & 0
\end{pmatrix} = A_\sigma
$$
Checking Homomorphism:
$f(\sigma \tau) = A_\sigma \cdot A_\tau$
$Image(f) =$ Permutation Matrices
$Ker(f) = \{e\}$

**Note that: $det(f(\sigma)) = \pm 1$**
If $det(f(\sigma)) = 1$, then it is an even permutation and if $det(f(\sigma)) = -1$, then it is an odd permutation.
**Note that: $A_n = Kernel = \{\sigma: det(f(\sigma)) = 1\} \lhd S_n$. Also known as the Even Permutations.**

### Checking Isomorphism
**Properties**
1. $|G_1| = |G_2|$
2. $G_1$ is abelian $\iff$ $G_2$ is abelian
3. $G_1$ and $G_2$ have the same number of elements of every order. 
4. Check if the Image $= G'$ and the Kernel $= \{e\}$.
	1. If $G = G'$ and $f$ is an isomorphism, then we say that $G$ is an automorphism.

### [[Automorphism]]
**The Structure preserving the symmetries of $G$.**
*Inverses are Automorphisms*

### Ur Group
$Sym(T) = \{ \text{all bijections from T} \rightarrow \text{T} \} = Automorphism$ $Group(T) = \{ \text{all automorphisms of the set } T \}$ 
1. $a \cdot b (t) = a(b(t))$
2. $e(t) = e$
3. $a^{-1}(a(t)) = t$

## Group Examples
### Symmetry Group
$S_n = Sym\{1,2,3, \ldots, n-1, n\} =$ permutation group on $n$ letters.
**FINITE** group with $|S_n| = n!$

$S_1 = \{e\}$

$S_2 = \{e, \tau\}$ where $\tau$ maps $1 \rightarrow 2$ and $2 \rightarrow 1$. (Abelian)
- $e\tau = \tau e = \tau$
- $\tau \tau = e$
- $\tau = \tau^{-1}$

$S_3 = \{e, \tau, \tau', \tau'', \sigma, \sigma'\}$ where $\tau$ is a **transposition** (exchange two elements - inverse of transposition is itself)
$\tau \sigma(2) = \tau(\sigma(1)) = \tau(2) = 1 = \tau'$
$\sigma\tau(1) = \sigma(2) = 3 = \tau''$
$\therefore S_3$ is not abelian.
#### Pictures
![[Pasted image 20220223083409.png]]
![[Pasted image 20220223083527.png]]



#### The Group $S_n$ for $n \geq 3$ is non-abelian
Prove that $S_3$ is a subgroup of $S_n$ for $n \geq 3$ which fixes $S_n$ for $n \geq 3$. 

For $k \leq n$, $S_k \subset S_n$. 

### [[Equivalence Relations]]
#### Sets
A *partition*, $\Pi$, of a set $S$ is a subdivision of $S$ into non-overlapping, nonempty subsets. Different Subsets are called the Equivalence Classes.

3 Properties
1. For all $a$, $a \sim a$
2. $a \sim b \rightarrow b \sim a$ 
3. $a \sim b$ and $b \sim a \rightarrow a \sim c$

Can think of an Equivalence Relation as a Partition of $S \times S$.

Note that $a \equiv b \text{ mod } n$ is a synonym for $a \sim b$ with $n$ made explicit.

#### Groups
Suppose $f: G \rightarrow G'$ be a group homomorphism where $H \lhd G$ be the kernel of $f$.
*We get an equivalence relation on $G$, where $H$ is one of the equivalence classes.* This is because $H = f^{-1}(e') = \{a \in G: f(a) = f(e) = e'\}$.

The other equivalence classes have the form $aH = \{ah: h \in H\}$.

**Equivalence Classes for a homomorphisms of a Group are all of the different left cosets of the Kernel.**

### Cosets
**$aH = \{ah: h \in H\}$ is the left coset of  $H$ in $G$.**

**For a Group Homomorphism, all of the left cosets are of the same size.**

If $G$ is finite and $f: G \rightarrow G'$ with kernel $H$, then: 
$|G| = |H| \cdot |Image(f)|$ 

#### Index
We define the Index of $H$ as the number of distinct left cosets (Or the number of equivalence Classes). $[G:H]$ or $(G:H)$ 

**$|G| = |H| \cdot [G:H]$** because we've divided $G$ into equal parts (the number of parts is the Index) and the number of elements is the order of $H$.

##### Lagrange's Theorem
If $|G|$ is finite and $g \in G$, then the order of $g$ divides $|G|$.

If $G$ is a finite group, with $|G| = p$ where $p$ is a prime number, then $G$ is cyclic generated by any $g \in G$ with $g \neq e$. Furthermore, the only subgroups of $G$ are $e$ and $G$.

##### Simple Groups
A group $G$ is simple if its only normal subgroup $H$ are $e$ and $G$.

1. Any $G$ of prime order $p$ is simple.
2. $A_n$ is simple for $n \geq 5$
 
##### Quotient Group
$G/H = \text{ set of all cosets } aH$.

