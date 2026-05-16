Leontief economic [[mathematical model|model]]

The basis of the model is as follows:
- The economy can be divided into 500 sectors 
- Each section has an equation relating showing distribution of a single unit of output amongst other sectors.
Suppose that for each sector, we know the total output for 1 year, and we know now this output maps to other areas of the economy. Let the total dollar value of a sector be called the *price* of that amount. 
There exists equilibrium prices that can be assigned to the total outputs of the various sectors in such a way that the income of each sector exactly balances its expenses. 


For this system, $C$, the matrix, denotes the consumption matrix. Its entry Its entry $c_{ij}$​ is the amount of sector $i$'s output required as input to produce *one unit* of sector $j$'s output.
The augmented column, $b$, is what what is the leaves the system to consumers. The vector $\vec{x}$ is everything the system has to churn out so that b can leave it. 




# closed economic model 
Every column tells you *one* unit of output. Each entry in the column builds up to the total(all entries in a column sum to one).
We set up a linear system as follows. 
Suppose each year, we have 3 sectors, agriculture, manufacturing and services denoted $a,m,s$ with the following equations. 
$x_{a}=ax_{a}+bx_{m}+cx_{s}$
we create a [[Transition Matrix]]
  A     M    S
$\begin{bmatrix}0.0\ \   0.4\ \ 0.6 |A \\ \ \  0.6  \ \ 0.1 \ \ 0.2 |M\ \  \\0.4\ \ 0.5\ \ 0.2| S\end{bmatrix}$
An important [[theorem]]:
If the columns of C add up to 1, then $(I_{n}-C)\begin{pmatrix}x_{1} \\ x_{2} \\ x_{3}\end{pmatrix}$ is *not* invertible. If ($I_{n}-c$) is not invertible, then there is no solution. Recall this from [[Proving an Inverse matrix]].
# productive economic model  
A productive model is where it requires less than one unit of total input(sum of column) to get a single unit of output. Suppose we have a productive economy, where every column sums to less than 1.

$\begin{bmatrix}b_{a} \\ b_{m}  \\b_{s}\end{bmatrix} = \begin{bmatrix} x_{a}  \\ x_{m}  \\ x_{s}\end{bmatrix}- \begin{bmatrix}0.1\ \  0.2\ \ 0.3  \\ 0.3 \ \ 0.2\ \ 0.2  \\ 0.5 \ \ 0.3\ \ 0.1\end{bmatrix} \cdot \begin{bmatrix}x_{a}  \\  x_{m}  \\ x_{s}\end{bmatrix}$
$\ \ \ \vec{b}\ \ \ \   =\ \ \ \ \ \ \ \  \vec{x} - \ \ \ \ \ \ \ \ \ \ c \ \ \ \ \ \ \ \ \ \ \times\ \ \ \ \ \ \ \ \ \vec{x}$     

This equation above is finding the amount of output required for a certain surplus to be present. 
$\vec{x}$ is what was produced, $C \vec{x}$ is how much of that output got consumed by production, thus $\vec{x}-C \vec{x}$ gives the output-input, or surplus ($\vec{b}$)

Extending the [[theorem]]
If all columns of a matrix C do not add up to 1, then $I_{n}-c$ is invertible, thus there exists a unique solution. 

Using this:
suppose we want to produced 60 000 dollars worth of surplus of manufacturing, and 30,000 dollars worth of surplus from services

$\begin{bmatrix}30 \\ 60\end{bmatrix} = \begin{bmatrix} x_{a}  \\ x_{m}  \\ \end{bmatrix}- \begin{bmatrix}0.1\ \  0.2  \\ 0.5 \ \ 0.5\end{bmatrix} \cdot \begin{bmatrix}x_{a}  \\  x_{m}\end{bmatrix}$
For this model, as long as $x_{a}$ and $x_{m}$ are not negative, we can say that there is a solution. There is not simple theorem we can use for this, as the columns are neither summing to 1 or less than 1, so the previous theorems do not apply. The only way to do this is to solve it. 
$(\begin{bmatrix} 10 \\ 01\end{bmatrix}-\begin{bmatrix}0.1\ \  0.2  \\ 0.5 \ \ 0.5\end{bmatrix})\cdot \begin{bmatrix}x_{a} \\ x_{m}\end{bmatrix}=\begin{bmatrix}30  \\ 60\end{bmatrix}$
Note that the first matrix is the [[Identity matrix]].
