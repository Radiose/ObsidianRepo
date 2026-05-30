- Statement: A sentence that is **either** true or false, but not both.
- Compound statements: built using [[logical connective]]s
- P is a sufficient condition for Q means $p \implies q$
- P is a necessary condition for Q means $\neg p \implies \neg q$
- Predicate: a sentence containing one or more variables with the property that, when a value from a specified domain is given to each variable, the sentence becomes a [[Statement]]. The specified domain is the domain of the predicate.

- Pairwise disjoint: Two [[set]]s are **disjoint** when $a \cap B = \emptyset$. This means that there are no elements in both sets. 
	Given a set of sets $\mathcal{S}$, the sets in S are said to be in pairwise disjoint when 
	$\forall a,b \subset S | a\not=b$ and $a \cap b = \emptyset$
- Axiom of extensionality: A [set](app://obsidian.md/set) is defined solely by the elements that comprise it .                     
	No importance is given to order or frequency of elements

-  A is a **partition** of S when each of the following are true:
	1: $\emptyset \not\in A$
	2: every element of S is an element of some set in A. 
	ie $\forall s \in S, \ \  \exists A \in A$   $s\in A$. Think about this as: a partition is a set of sets, with its elements ([[set]]s) being also sets in S ([[powerset]]s).
	3: The sets in A are pairwise disjoint
	
- subsets $a \subset b \iff \forall x(x\in a \implies x\in b)$

- Given (not necessarily distinct) sets $A_{1}$, $A_{2}$, . . . , $A_{n}$, the Cartesian
	product of $A_{1}, A_{2}$, . . . , $A_{n}$, denoted $A_{1} × A_{2} × · · · × A_{n}$, is the set of all
	ordered n-tuples ($a_{1}, a_{2}, . . . , a_{n}$) where $a_{1}$ ∈ $A_{1}$, $a_{2} ∈ A_{2}$, . . . ,$a_{n} ∈ A_{n}.$


- relation: let A,B be non empty [[set]]s. Any [[subset]] of AxB is called a relation from A to B. A relation from A to A is called a relation on A. A [[Cartesian product]]s subset is a relation

- $r^{-1}=\{ (b,a)\in B\times A|(a,b) \in R \}$
	the inverse relation $r^{-1}\subset B\times A$
	thus $b R^{-1}a \iff a Rb$

- reflexive [[relation]]
	Let S be a set and let ~ be a relation on S. We say that
	~ is reflexive when $\forall s \in S s$ ~$s$ 
	This means every element is related to itself. The less than relation is not reflexive. The less than or equal to relation on the set of integers is reflexive.

- symmetric [[relation]]
	~ is symmetric when $\forall s,\ t \in S\ s$~$t \to t$~$s$ 
	This means every element of s is related to t, and that t is related to s.
	The less than or equal to is not symmetric. 6 is less than or equal to 7, but 7 is not less than or equal to 6.

- an equivalence relation is a [[reflexive relation]], [[transitive relation]] [[symmetric relation]]. This means that it could serve as your idea of somethings being the same.

- We say that the [[relation]] is antisymmetric when $\forall s,t \in S((s \textasciitilde t)\land (t \textasciitilde s) \to s = t)$

- Partial order If ~ is a [[reflexive relation]], a [[transitive relation]] and asymmetric, then we say that ~ is a partial order on s.


- Function: 
	- let A,B be sets. A [[relation]] F from A to B is called a function from A to B when $\forall a \in A \exists!b\in B (a,b) \in f$

- injective: $\forall a_{1},a_{2} \in A(a_{1} \not=a_{2}) \implies f(a_{1})\not=f(a_{2})$
- surjective  $\forall b \in B \exists a \in A f(a)=b$.
- bijection - injective and surjective OR $∀y∈B, ∃!x∈A, f(x)=y$






Mistakes: 
Probability:
x OR y - likely exlusive or - remember to subtract p(x^y)
Estimate vs exact - makes difference between independence of two random variables 

Don’t forget that every set has itself and the empty set as subsets.
The number of subgraphs can be determined by fixing the number of vertices and counting the amount of possible edges 