Markov process 
A Markov process is a process that using probabilities can be modelled. 
# Requirements of a Markov process
- a finite number of states
- moves between states in a time step 
- Uses discrete time 
The Markov process will tell you if the system runs for n steps, what is the probability the system is in this state? 

A discrete [[Markov process]] has probabilities of being at a specific time depends on:
Its state at the (n-1) timestep. 
A fixed stochastic matrix, $T \in M_{k}(\mathbb{Q}_{\ge {0}})$ labelled the [[Transition Matrix]]. 

## Some terminology
- Probability [[vector]]: has non negative entries that sum to 1
- Stochastic matrix: square matrix such that all columns are probability vectors. Is denoted as positive if all entries are non zero. Denoted as T. 
- ![[Steady state vector]]
Perron-Frobenius [[theorem]]:
Let T be a stochastic matrix. If T, or some power of T is a positive matrix, then 

- there exists a unique steady state probability vector V with respect to T
- as $n \to \infty$, $T^n$ converges to the $n \times n$ [[Matrix]] where all columns are V 
- For any initial probability vector, the [[Sequence]] $V_{0}, TV_{0},T^2V_{0}\dots$ converges to V 

