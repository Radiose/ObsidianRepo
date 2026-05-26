Blood glucose [[mathematical model|model]]


 A glucose solution is administered intravenously into the bloodstream at a constant rate r. As the glucose is added, it is converted into other substances and removed from the bloodstream at a rate that is proportional to the concentration at that time.
- Make a model of the concentration of glucose solution in the
	bloodstream over time.
- Solve your model to express the concentration of glucose solution in the
	bloodstream as a function of time.
- Use your model to predict the long-term concentration of glucose
	solution in the bloodstream and interpret your answer.

### Making the model 
We note 3 key pieces of information: 
- Administered at a constant rate r 
- removed from blood at a rate that is proportional to the concentration of at the time 
- there is no initial solution in the body 
We have rates here, so we can create an [[ordinary differential equation]] that's both an [[Initial value problem]] as well as a [[Separable ODE]]
$\frac{dC}{dt}=r-kc$ and $C_{0}=0$
$\implies \int\frac{1}{r-kc}dc=\int 1dt$
$\implies-\frac{1}{k}\ln|r-kC|=t+b_{1}$ (left int done with u sub)
$\implies \ln|r-kC|=-kt+b_{2}$
$\implies e^{\ln|r-kC|} =e^{-kt+b_{2}}$
$\implies |r-kC|=b_{3}e^{-kt}$
$\implies kC =r-B_{4}e^{-kt}$
$\implies C = \frac{r}{k} − B_{5}e^{-kt}$

We then solve for B5 using the initial value 
We then understand long term behaviour via finding convergence when via $\lim_{ t \to \infty } C(t)$

