Proving quantifies

To prove $\forall xp(x)$, create a fixed but arbitrary variable of the [[predicate]] domain and argue that p(x) is true.


To prove $\exists xp(x)$, show any variable that applies in the predicate domain.

Note that you cannot simply state the variable in the domain, you have to *show* how the variable is valid. 
Example: prove ![[The conditional statement]]$x^2-6x+8 =0$ has an integer solution
This can be interpreted as an $\exists$ [[Statement]]. 
The [[proof]] can be as simple as when x=2, the left hand side of the equation evaluates to ... which equals 0.


 
To disprove a for all statement, create an example that evaluates to false. 
Disproving a $\forall$ statement is proving the negation. This is because $\neg(\forall p(x)) \equiv \exists x\neg p(x)$
This is called providing a **counterexample**. 

For example: For every integer x, $(x-1)^2+(x+1)$ is positive.
This statement is false because x = 0 is a counterexample.
blah blah 0 is not positive. 


To disprove an exists statement, prove the negation ($\forall x\neg(p(x))$).
For example:
 
$\exists y \forall x (y \le x)$ , where the [[quantification]] is over the set of integers. 
This statement above is essentially claiming that there exists an integer y, that is greater than or equal to every integer. 
This statement is obviously false
proof
$\neg(\exists y\forall x(y \le x)) \equiv \forall x \exists y(y > x)$
Let y be an integer, and let x = y-1. It is clear that y>x.


Proving and disproving a statement is significantly easier when you quantify the predicate with exists and for all statements. 
Respond to the statement with a [[logical structure of a proof]].