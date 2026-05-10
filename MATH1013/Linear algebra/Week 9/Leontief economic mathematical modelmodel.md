Leontief economic [[mathematical model|model]]

The basis of the model is as follows:
- The economy can be divided into 500 sectors 
- Each section has an equation relating showing distribution of a single unit of output amongst other sectors.
Suppose that for each sector, we know the total output for 1 year, and we know now this output maps to other areas of the economy. Let the total dollar value of a sector be called the *price* of that amount. 
There exists equilibrium prices that can be assigned to the total outputs of the various sectors in such a way that the income of each sector exactly balances its expenses. 

# closed economic model 
Every column tells you *one* unit of output. Each entry in the column builds up to the total(all entries in a column sum to one).
We set up a linear system as follows. 
Suppose each year, we have 3 sectors, agriculture, manufacturing and services denoted $a,m,s$ with the following equations. 
$x_{a}=ax_{a}+bx_{m}+cx_{s}$
we create a [[Transition Matrix]]
  A     M    S
$\begin{bmatrix}0.0\ \   0.4\ \ 0.6 |A \\ \ \  0.6  \ \ 0.1 \ \ 0.2 |M\ \  \\0.4\ \ 0.5\ \ 0.2| S\end{bmatrix}$
An important [[theorem]]:
If the columns of C add up to 1, then $(I_{n}-C)\begin{pmatrix}x_{1} \\ x_{2} \\ x_{3}\end{pmatrix}$ is *not* invertible 
# productive economic model  
A productive model is where it requires less than one unit of total input(sum of column) to get a single unit of output. Suppose we have a productive economy, where every column sums to less than 1.

$\begin{bmatrix}b_{a} \\ b_{m}  \\b_{s}\end{bmatrix} = \begin{bmatrix} x_{a}  \\ x_{m}  \\ x_{s}\end{bmatrix}- \begin{bmatrix}0.1\ \  0.2\ \ 0.3  \\ 0.3 \ \ 0.2\ \ 0.2  \\ 0.5 \ \ 0.3\ \ 0.1\end{bmatrix} \cdot \begin{bmatrix}x_{a}  \\  x_{m}  \\ x_{s}\end{bmatrix}$
$\ \ \ \vec{b}\ \ \ \   =\ \ \ \ \ \ \ \  \vec{x} - \ \ \ \ \ \ \ \ \ \ c \ \ \ \ \ \ \ \ \ \ \times\ \ \ \ \ \ \ \ \ \vec{x}$     

