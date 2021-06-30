# Column generation for cutting stock problem
This is a example of solving 1-D cutting stock problem by column generation.


There are two class: MasterProblem and SlaveProblem obtained by Dantzig-Wolfe decomposition.

Master problem has a formulation like:
```math
e^i + 1 = 0
```
