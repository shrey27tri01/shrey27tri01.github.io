---
layout: project
title: Degrees of Separation
subtitle: Determine the degrees of separation of two actors
---

Program to determine the degrees of separation of two actors, inspired by the game [6 degrees of Kevin Bacon](https://en.wikipedia.org/wiki/Six_Degrees_of_Kevin_Bacon).   

The degree of separation between two actors is determined by the shortest sequence of movies that connects them. For example, Tom Cruise and Michael Caine are separated by a degree of 2, since they are connected by a sequence of minimum 2 movies: Tom Cruise and Sean Connery starred in "Close Up", and Sean Connery and Michael Caine starred in "A Bridge Too Far".  

The degree of separation is calculated by calculating the shortest path between two actors using Breadth First Search (BFS) on a large dataset that consists of a number of actors and movies (credits [IMDb](https://www.imdb.com/)). Here, actors are thought of as "nodes" in a graph, and movies are the "edges". So, an edge connecting two nodes implies that the movie corresponding to that edge stars the respective actors corresponding to the nodes. 


#### Implementation:

[GitHub Repository](https://github.com/shrey27tri01/degrees-of-separation)   




