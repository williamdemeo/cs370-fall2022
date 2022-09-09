# CS 370: Introduction to Artificial Intelligence, Spring 2022

# Project 1. Search

**Due: Fri 18 Feb 2022 by 11:59 pm**

<img src="https://github.com/williamdemeo/cs370-spring2022/blob/master/projects/Project1/pacman.png" alt="Pacman maze" class="center-image img-fluid" style="width: 400px;" />

All those colored walls,  
Mazes give Pacman the blues,  
So teach him to search.

-----------------------------------------

## Introduction

In this project, your Pacman agent will find paths through his maze world, both to reach a particular location and to collect food efficiently. You will build general search algorithms and apply them to Pacman scenarios.

As in Project 0, this project includes an autograder for you to grade your answers on your machine. This can be run with the command:

`python autograder.py`

See the autograder tutorial in Project 0 for more information about using the autograder.

The code for this project consists of several Python files, some of which you will need to read and understand in order to complete the assignment, and some of which you can ignore.  You can download all the code and supporting files as a [zip archive][].

**IMPORTANT!**

Please keep in mind the information displayed in the following tables.  Use it to guide your coding effort and help you avoid doing unnecessary work.

| **Files you'll edit** | **Description**                                    |
|-----------------------|----------------------------------------------------|
| `search.py`           | Where all of your search algorithms will reside.   |
| `searchAgents.py`     | Where all of your search-based agents will reside. |


| **Files you might look at** | **Description**                                            |
|-------------------------------------|------------------------------------------------------------|
| `pacman.py`                         | Main file that runs Pacman games and describes Pacman GameState type used in this project. |
| `game.py`                           | The logic behind how the Pacman world works. This file describes several supporting types like `AgentState`, `Agent`, `Direction`, and `Grid`. |
| `util.py`                           | Useful data structures for implementing search algorithms. |


| **Supporting files you can ignore** | **Description**                                          |
|-------------------------------------|----------------------------------------------------------|
| `graphicsDisplay.py`                | Graphics for Pacman                                      |
| `graphicsUtils.py`                  | Support for Pacman graphics                              |
| `textDisplay.py`                    | ASCII graphics for Pacman                                |
| `ghostAgents.py`                    | Agents to control ghosts                                 |
| `keyboardAgents.py`                 | Keyboard interfaces to control Pacman                    |
| `layout.py`                         | Code for reading layout files and storing their contents |
| `autograder.py`                     | Project autograder                                       |
| `testParser.py`                     | Parses autograder test and solution files                |
| `testClasses.py`                    | General autograding test classes                         |
| `test_cases/`                       | Directory containing the test cases for each question    |
| `searchTestClasses.py`              | Project 1 specific autograding test classes              |


**Files to Edit and Submit**. You will fill in portions of `search.py` and `searchAgents.py` during 
the assignment. Once you have completed the assignment, you will submit a token generated by `autograder.py`.
Please *do not* change the other files in this distribution or submit any of our original files other than these files.

**Evaluation**. Your code will be autograded for technical correctness. Please *do not* change the names of any provided functions or classes within the code, or you will wreak havoc on the autograder. However, the correctness of your implementation---not the autograder's judgments---will be the final judge of your score. If necessary, we will review and grade assignments individually to ensure that you receive due credit for your work.

**Academic Dishonesty**. We will be checking your code against other submissions in the class for logical redundancy. If you copy someone else's code and submit it with minor changes, we will know. These cheat detectors are quite hard to fool, so please don't try. We trust you all to submit your own work only; *please* don't let us down. If you do, we will pursue the strongest consequences available to us.

**Getting Help**. You are not alone! If you find yourself stuck on something, contact the course staff for help. Office hours and the discussion forum are there for your support; please use them. If you can't make our office hours, let us know and we will schedule more. We want these projects to be rewarding and instructional, not frustrating and demoralizing. But, we don't know when or how to help unless you ask.

**Discussion**. Please be careful not to post spoilers.

-----------------------------------------

## Welcome to Pacman

After downloading the code ([search.zip][]), unzipping it, and changing to the directory, you should be able to play a game of Pacman by typing the following at the command line:

```shell
python pacman.py
```

Pacman lives in a shiny blue world of twisting corridors and tasty round treats. Navigating this world efficiently will be Pacman's first step in mastering his domain.

The simplest agent in `searchAgents.py` is called the `GoWestAgent`, which always goes West (a trivial reflex agent). This agent can occasionally win:

```shell
python pacman.py --layout testMaze --pacman GoWestAgent
```

But, things get ugly for this agent when turning is required:

```shell
python pacman.py --layout tinyMaze --pacman GoWestAgent
```

If Pacman gets stuck, you can exit the game by typing `CTRL-c` into your terminal.

Soon, your agent will solve not only `tinyMaze`, but any maze you want.

Note that `pacman.py` supports a number of options that can each be expressed in a long way (e.g., `--layout`) or a short way (e.g., `-l`). You can see the list of all options and their default values via:

```shell
python pacman.py -h
```

Also, all of the commands that appear in this project also appear in `commands.txt`, for easy copying and pasting. In UNIX/Mac OS X, you can even run all these commands in order with `bash commands.txt`.

-------------------

## New Syntax

You may not have seen this syntax before:

```python
def my_function(a: int, b: Tuple[int, int], c: List[List], d: Any, e: float=1.0):
```

This is annotating the type of the arguments that Python should expect for this function. In the example below, `a` should be an `int` (integer), `b` should be a `tuple` of 2 `int`s, `c` should be a `List` of `List`s of anything (i.e., a 2D array of anything), `d` is essentially the same as not annotated and can by anything, and `e` should be a `float`. Also, `e` is set to a default value of 1.0 if nothing is passed in for it.

For example, the call

```python
my_function(1, (2, 3), [['a', 'b'], [None, my_class], [[]]], ('h', 1))
```

fits the type annotations, and doesn't pass anything in for `e`, so `e` is set equal to 1.0.

Type annotations (along with docstrings) help you know what argument types the function takes as input. Python itself doesn't enforce these. When writing your own functions, it is up to you if you want to annotate your types; they can be very helpful, but your program may be simple enough that you don't want to bother with them.

-----------

## Question 1 (3 points): Finding a Fixed Food Dot using Depth First Search

In `searchAgents.py`, you'll find a fully implemented `SearchAgent`, which plans out a path through Pacman's world and then executes that path step-by-step. The search algorithms for formulating a plan are not implemented---that's your job.

First, test that the `SearchAgent` is working correctly by running:

```shell
python pacman.py -l tinyMaze -p SearchAgent -a fn=tinyMazeSearch
```

The command above tells the `SearchAgent` to use `tinyMazeSearch` as its search algorithm, which is implemented in `search.py`. Pacman should navigate the maze successfully.

Now it's time to write full-fledged generic search functions to help Pacman plan routes! Pseudocode for the search algorithms you'll write can be found in the lecture slides. Remember that a search node must contain not only a state but also the information necessary to reconstruct the path (plan) which gets to that state.

**Important note**. All of your search functions need to return a list of *actions* that will lead the agent from the start to the goal. These actions all have to be legal moves (valid directions, no moving through walls).

**Important note**. Make sure to use the `Stack`, `Queue` and `PriorityQueue` data structures provided to you in `util.py`! These data structure implementations have particular properties which are required for compatibility with the autograder.

*Hint*. Each algorithm is very similar. Algorithms for DFS, BFS, UCS, and A* differ only in the details of how the fringe is managed. So, concentrate on getting DFS right and the rest should be relatively straightforward. Indeed, one possible implementation requires only a single generic search method which is configured with an algorithm-specific queuing strategy. (Your implementation need not be of this form to receive full credit).

Implement the depth-first search (DFS) algorithm in the `depthFirstSearch` function in `search.py`. To make your algorithm *complete*, write the graph search version of DFS, which avoids expanding any already visited states.

Your code should quickly find a solution for:

```shell
python pacman.py -l tinyMaze -p SearchAgent
```

```shell
python pacman.py -l mediumMaze -p SearchAgent
```

```shell
python pacman.py -l bigMaze -z .5 -p SearchAgent
```

The Pacman board will show an overlay of the states explored, and the order in which they were explored (brighter red means earlier exploration). Is the exploration order what you would have expected? Does Pacman actually go to all the explored squares on his way to the goal?

*Hint*. If you use a `Stack` as your data structure, the solution found by your DFS algorithm for `mediumMaze` should have a length of 130 (provided you push successors onto the fringe in the order provided by getSuccessors; you might get 246 if you push them in the reverse order). Is this a least cost solution? If not, think about what depth-first search is doing wrong.

*Grading:* Please run the command below to see if your implementation passes all the autograder test cases for Question 1.

```shell
python autograder.py -q q1
```

-----------------------

## Question 2 (3 points): Breadth First Search

Implement the breadth-first search (BFS) algorithm in the `breadthFirstSearch` function in `search.py`. Again, write a graph search algorithm that avoids expanding any already visited states. Test your code the same way you did for depth-first search.

```shell
python pacman.py -l mediumMaze -p SearchAgent -a fn=bfs
```

```shell
python pacman.py -l bigMaze -p SearchAgent -a fn=bfs -z .5
```

Does BFS find a least cost solution? If not, check your implementation.

*Hint*. If Pacman moves too slowly for you, try the option `--frameTime 0`.

*Note*. If you've written your search code generically, your code should work equally well for the eight-puzzle search problem without any changes.

```shell
python eightpuzzle.py
```

*Grading:* Please run the below command to see if your implementation passes all the autograder test cases for Question 2.

```shell
python autograder.py -q q2
```

-----------------------

## Question 3 (3 points): Varying the Cost Function

While BFS will find a fewest-actions path to the goal, we might want to find paths that are "best" in other senses. Consider `mediumDottedMaze` and `mediumScaryMaze`.

By changing the cost function, we can encourage Pacman to find different paths. For example, we can charge more for dangerous steps in ghost-ridden areas or less for steps in food-rich areas, and a rational Pacman agent should adjust its behavior in response.

Implement the uniform-cost graph search algorithm in the `uniformCostSearch` function in `search.py`. We encourage you to look through `util.py` for some data structures that may be useful in your implementation. You should now observe successful behavior in all three of the following layouts, where the agents below are all UCS agents that differ only in the cost function they use (the agents and cost functions are written for you):

```shell
python pacman.py -l mediumMaze -p SearchAgent -a fn=ucs
```

```shell
python pacman.py -l mediumDottedMaze -p StayEastSearchAgent
```

```shell
python pacman.py -l mediumScaryMaze -p StayWestSearchAgent
```

*Note*. You should get very low and very high path costs for the `StayEastSearchAgent` and `StayWestSearchAgent` respectively, due to their exponential cost functions (see `searchAgents.py` for details).

*Grading*. Please run the below command to see if your implementation passes all the autograder test cases.

```shell
python autograder.py -q q3
```

---------------------------

## Question 4 (3 points): A* search

Implement A* graph search in the empty function `aStarSearch` in `search.py`. A* takes a heuristic function as an argument. Heuristics take two arguments: a state in the search problem (the main argument), and the problem itself (for reference information). The `nullHeuristic` heuristic function in `search.py` is a trivial example.

You can test your A* implementation on the original problem of finding a path through a maze to a fixed position using the Manhattan distance heuristic (implemented already as `manhattanHeuristic` in `searchAgents.py`).

```shell
python pacman.py -l bigMaze -z .5 -p SearchAgent -a fn=astar,heuristic=manhattanHeuristic
```

You should see that A* finds the optimal solution slightly faster than uniform cost search (about 549 vs. 620 search nodes expanded in our implementation, but ties in priority may make your numbers differ slightly). What happens on `openMaze` for the various search strategies?

*Grading*. Please run the below command to see if your implementation passes all the autograder test cases for Question 4.

```shell
python autograder.py -q q4
```

-------------------------------

## Submission

In order to submit your project, run `python autograder.py` and, when you are satisfied with the results, submit the file `search.py`, and (if you modified them) the files `searchAgents.py` and `util.py`, to the `Project 1` assignment on Gradescope.

Please note: if you modified files other than these three, and if your solution depends on those modifications, then it is likely that your submission will not be accepted.  Please limit your code to the files `search.py`, `searchAgents.py`, and `util.py` (though it is possible to achieve a full score on this assignment by modifying only a subset of the three files mentioned).

-------------------------------------------

## Attribution

This page and the project it describes were adapted from similar materials at [https://inst.eecs.berkeley.edu/~cs188/sp22/project1/](https://inst.eecs.berkeley.edu/~cs188/sp22/project1/), which the dedicated folks at [ai.berkeley.edu](http://ai.berkeley.edu/home.html) have generously made available for reuse.

[zip archive]: https://github.com/williamdemeo/cs370-spring2022/raw/master/projects/Project1/search.zip
[search.zip]: https://github.com/williamdemeo/cs370-spring2022/raw/master/projects/Project1/search.zip