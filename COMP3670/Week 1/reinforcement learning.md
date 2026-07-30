Generally thought of as some mode of learning in between [[supervised learning]] and [[unsupervised learning]]. 
The general idea is that we have some grade for correctness instead of a blank yes/no answer. 

An agent observes a state $\mathbf{x}$, takes an **action**, and receives some reward signal (grade). 

Some examples are chess - with $\mathbf{x}$ representing the state of the board. +1 for winning, -1 for losing and 0 for not ending a game with a move. 

The agent must figure out what moves were responsible for winning or losing after each game. 

Another example is an algorithm - with the state being the user profile, time of day and watch history, and the action is recommending a video to watch and the reward is user clicks and watch time, which is some grade. 