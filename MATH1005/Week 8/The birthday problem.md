This is a classic thought experiment that can be proven with basic [[Probability rules]] as well as counting.
In a room full of 50 people, what is the likelihood that at least two share a birthday?

We will solve this via proving the complement IE, what is the likelihood that none share a birthday?
Well, to do this, we want to think about how many ways the 50 birthdays can be shown without there being a repeat in the [[sequence]].
This leads to the [[permutation]]. We are trying to determine how many distinct ways to order 50 birthdays. 
Great, so now we want to find the [[Probability of an event]]. We must determine the [[Sample space]].

How many ways are there to get 50 birthdays out of 365(with repeats)? Simple, $365^{50}$.
Thus, the answer is  $1 -\frac{P(365,50)}{365^50}$

