homogenous system of linear equations 
A homogenous system of linear equations is one in the form Ax = 0. In this case, there is always the trivial solution x = 0.

Suppose $\vec{x}_{0}$ is a solution to $A \vec{x} = \vec{b}$ then any other solution of $A \vec{x}=\vec{b}$ must be in the format $\vec{x}=\vec{x}_{0}+v$ where $A \vec{v}=\vec{0}$ 

Also can be written as 
If p is any solution to the equation Ax = b, then the solutions of Ax = b are all vectors of the
form p + h where h is any solution of the homogeneous equation Ax = 0.

Imagine this with two parallel lines, each indicating a solution set. ![[Pasted image 20260311185712.png]]

The line going through the origin is A$\vec{v}$ = 0. The line above is Ax = b with the solution $x_{0}$. Any other solution of Ax = b, must hold the constraint that x = $x_{0}$ + v


### Remember
ax = 0 is always a [[Consistent linear system]], but ax = b might not be consistent. Ensure that its consistent before you start checking for solutions. 

## explanation by claude: 

Take **any** solution x on the Ax=b line. Then:

Ax=b and A$x_{0}$​=b

Subtract them:

A(x−x0)=b−b=0

So **(x - x₀) is automatically a homogeneous solution** — no choice, it's forced by the algebra.

$x=x_{0}+(x-x_{0})$​​
and because (x-x0) are solutions, they fit on the 0 line. So therefore 
$\vec{x} = \vec{x}_{0}+\vec{v}$ such that $A\vec{v}=0$ 

Every point on the Ax=b line is "secretly" just x₀ plus something that solves Ax=0. Not because we chose it that way — but because the **algebra forces it**.

The two lines are connected because **the difference between any two solutions always lands on the homogeneous line**. That's it.