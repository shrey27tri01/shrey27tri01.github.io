---
layout: project
title: Game Show
subtitle: A game show using sockets
---

A game show implemented in python using socket programming

#### Project Overview:
There is a host who conducts a game show and participants/players who provide answers. There are three participants. The host has a long list of questions and correct answers with him. He randomly chooses one of the questions (making sure it is not a repeat of previous questions) and sends to all three players. The players receive the question, think about the answer for a while and press the buzzer. There is a timer for 10 seconds for buzzer to be pressed. Otherwise, the host moves on to the next question. The first one to press the buzzer is given a chance to provide the answer within 10 seconds. If the answer is correct, he is given 1 point, otherwise -0.5. Nobody gets chance to answer this question again. The host then proceeds with the next question. The game stops when any player gets 5 points and that player is declared the winner. 
 
#### Description:
 I have divided the project into two phases, the client phase and the server phase. First, the server waits for a connection from the **four clients** (of which the players are three) and then proceeds with the questions only if all the participants have joined. Each of them has been assigned as Player1, Player 2 and Player 3 with respect to the time of their participation. Then the server broadcasts the questions from the stored set of questions in the list given by initiating the ​thread_function()​ function. It then waits for buzzer to be pressed from any one of the user and then waits for the user to give some input. If the user gives a correct answer his score is incremented accordingly and reduced if it is a wrong answer. It keeps on doing the process until a player scores 5 points. Then the program is ended. 
 
 You can find a live demo video of the project [here!](https://www.youtube.com/watch?v=ww9RosGTOBc&feature=youtu.be)

#### Implementation:

[GitHub Repository](https://github.com/shrey27tri01/Game-Show)




