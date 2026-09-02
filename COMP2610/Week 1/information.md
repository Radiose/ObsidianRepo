
information

This is the fundamental concept underpinning the course COMP2610. 
# Motivation

### Dictionary definition 
- facts provided or learned about something or someone 
- what is conveyed or represented by a particular arrangement or sequence of things 

### Definition in the course 
We think of information in this course as some rough measure of both the amount of unexpected data that some message contains, and how much the receivers uncertainty is reduced upon seeing the message. 

 The easiest method to quantify this uncertainty is to use [[Probability of an event|probability theory]]. Thus, it is essential in this course. 

### Information theory 
The study of the fundamental limits and potential of the representation and transmission of information. 

### Redundancy 
This is a fundamental concept involved in information theory. How can we transmit the most information using the least amount of medium? 


# Information content of an outcome 
The information content of an outcome relies on its probability. 
### Definition 
Let $X$ be a [[random variable]] with possible outcomes $\mathcal{X}$
let $p(x)$ denote the probability of an outcome $x \in \mathcal{X}$
The information outcome of an outcome $x \in \mathcal{X}$ is 

$$h(x)=\log_{2} \frac{1}{p(x)}$$
This is because the information content of something more unlikely will be larger, which is why its under 1.
In this case, we use $\log_{2}$ because we are using bits, but choice of base is still arbitrary. 

The *average* information content of a random variable is called the [[entropy (information theory)|entropy]] of a random variable. 