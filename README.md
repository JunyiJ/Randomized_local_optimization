# Randomized optimization and local search methods

## Random hill climbing

Hill Climbing is heuristic search used for **mathematical optimization problems** in the field of Artificial Intelligence.

Given a large set of inputs and a good **heuristic function**, it tries to find a sufficiently good solution to the problem. This solution may not be the **global optimal maximum**.


* In the above definition, **mathematical optimization** problems implies that hill climbing solves the problems where we need to maximize or minimize a given real function by choosing values from the given inputs. Example-Travelling salesman problem where we need to minimize the distance traveled by salesman.
* **Heuristic search** means that this search algorithm may not find the optimal solution to the problem. However, it will give a good solution in reasonable time.
* A heuristic function is a function that will rank all the possible alternatives at any branching step in search algorithm based on the available information. It helps the algorithm to select the best route out of possible routes.

<br>

![Random hill climbing](https://i.stack.imgur.com/HISbC.png)

## Simulated annealing

Simulated annealing (SA) is a **probabilistic technique** for approximating the global optimum of a given function. Specifically, it is a **metaheuristic to approximate global optimization in a large search space**. It is often used when the search space is discrete (e.g., all tours that visit a given set of cities). 

For problems where finding an approximate global optimum is more important than finding a precise local optimum in a fixed amount of time, simulated annealing may be preferable to alternatives such as gradient descent.

The name and inspiration come from annealing in **metallurgy**, a technique involving heating and controlled cooling of a material to increase the size of its crystals and reduce their defects. Both are attributes of the material that depend on its **thermodynamic free energy**. Heating and cooling the material affects both the temperature and the thermodynamic free energy. 

> ***The simulation of annealing can be used to find an approximation of a global minimum for a function with a large number of variables to the statistical mechanics of equilibration (annealing) of the mathematically equivalent artificial multiatomic system.***

This notion of slow cooling implemented in the simulated annealing algorithm is interpreted as a slow decrease in the probability of accepting worse solutions as the solution space is explored. **Accepting worse solutions is a fundamental property of metaheuristics because it allows for a more extensive search** for the global optimal solution. 

In general, the simulated annealing algorithms work as follows. At each time step, the algorithm randomly selects a solution close to the current one, measures its quality, and then decides to move to it or to stay with the current solution based on either one of two probabilities between which it chooses on the basis of the fact that the new solution is better or worse than the current one. During the search, the temperature is progressively decreased from an initial positive value to zero and affects the two probabilities: at each step, the probability of moving to a better new solution is either kept to 1 or is changed towards a positive value; instead, the probability of moving to a worse new solution is progressively changed towards zero. 

<br>

![Simulated annealing](https://upload.wikimedia.org/wikipedia/commons/d/d5/Hill_Climbing_with_Simulated_Annealing.gif)
