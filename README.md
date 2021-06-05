## Degrees of Separation

Program to determine the degrees of separation of two actors, inspired by the game [6 degrees of Kevin Bacon](https://en.wikipedia.org/wiki/Six_Degrees_of_Kevin_Bacon).   

The degree of separation between two actors is determined by the shortest sequence of movies that connects them. For example, Tom Cruise and Michael Caine are separated by a degree of 2, since they are connected by a sequence of minimum 2 movies: Tom Cruise and Sean Connery starred in "Close Up", and Sean Connery and Michael Caine starred in "A Bridge Too Far".  

The degree of separation is calculated by calculating the shortest path between two actors using Breadth First Search (BFS) on a large dataset that consists of a number of actors and movies (credits [IMDb](https://www.imdb.com/)). Here, actors are thought of as "nodes" in a graph, and movies are the "edges". So, an edge connecting two nodes implies that the movie corresponding to that edge stars the respective actors corresponding to the nodes.   

### Usage

The `large` folder contains a large dataset in the form of CSV files, for actors and movies. The `small` folder contains a much smaller dataset, to be used for testing\experimental purposes. To use either, just append the folder name to `python degrees.py`, as follows:  
```
$ python degrees.py large
Loading data...
Data loaded.

Name: Ian McKellen
Name: Jason Statham
2 degrees of separation.
1: Ian McKellen and Donald Sutherland starred in Six Degrees of Separation
2: Donald Sutherland and Jason Statham starred in The Mechanic

Name: Emma Watson
Name: Jennifer Lawrence
3 degrees of separation.
1: Emma Watson and Daniel Radcliffe starred in Harry Potter and the Goblet of Fire
2: Daniel Radcliffe and James McAvoy starred in Victor Frankenstein
3: James McAvoy and Jennifer Lawrence starred in Dark Phoenix
```

### Credits
[IMDb](https://www.imdb.com/), [CS50](https://learning.edx.org/course/course-v1:HarvardX+CS50AI+1T2020/home)