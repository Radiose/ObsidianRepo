Steady [[Transition Matrix|state vector]]:  vector V such that Tv = v

# Finding the [[Steady state vector]]:
In math1005, we find it by subtracting the identity matrix from the initial matrix, adding an augmented column for 0, then replacing the bottom row with all 1s(including the augmented section)

Mathematically, this is derived via 
$T \vec{v}=\vec{v}$
$\iff T \vec{v}-\vec{v}=0$
$\iff T \vec{v}-I \vec{v}=0$
$\iff (T-I) \vec{v}=0$
Use [[Row operation]] and gaussian elimination to solve.

