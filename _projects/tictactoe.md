---
layout: project
title: Tic Tac Toe
subtitle: A tic-tac-toe AI using the minimax algorithm
---

An AI to play tic-tac-toe, implemented using the minimax algorithm.  

The minimax algorithm is an adversarial brute force recursive search algorithm, where there are two players, one of which is trying to maximize a score, and the other is trying to minimize the score. The algorithm tries to optimize a player's move after considering all the possible states that the game can go through from that point onwards.  

In the case of tic-tac-toe, the algorithm tries to maximize the score for 'X', and tries to minimize the score for 'O'. 

Alpha-Beta pruning is a method to optimize the runtime of the minimax algorithm by terminating the evaluation of a move when it makes sure that it is worse than a previously examined move.   When added to the simple minimax algorithm, it gives the same output, but cuts off certain branches that can't possibly affect the final decision, hence dramatically improving the perfomance. 

#### Implementation:

[GitHub Repository](https://github.com/shrey27tri01/tic-tac-toe)




