# Column generation for cutting stock problem
This is a example of solving 1-D cutting stock problem by column generation.


There are two class: MasterProblem and SlaveProblem obtained by Dantzig-Wolfe decomposition.

Master problem has a formulation like:\n\n
<a href="https://www.codecogs.com/eqnedit.php?latex=min&space;\;z&space;=&space;\sum_{j=1}^{n}&space;x_{j}&space;\\&space;\sum_{j=1}^{n}&space;a_{ijxj}&space;\ge&space;d_{i}&space;\qquad&space;i&space;=&space;1,&space;...,m&space;\\&space;x_{j}&space;\ge&space;0&space;\qquad&space;i&space;=&space;1,&space;...,n" target="_blank"><img src="https://latex.codecogs.com/gif.latex?min&space;\;z&space;=&space;\sum_{j=1}^{n}&space;x_{j}&space;\\&space;\sum_{j=1}^{n}&space;a_{ijxj}&space;\ge&space;d_{i}&space;\qquad&space;i&space;=&space;1,&space;...,m&space;\\&space;x_{j}&space;\ge&space;0&space;\qquad&space;i&space;=&space;1,&space;...,n" title="min \;z = \sum_{j=1}^{n} x_{j} \\ \sum_{j=1}^{n} a_{ijxj} \ge d_{i} \qquad i = 1, ...,m \\ x_{j} \ge 0 \qquad i = 1, ...,n" /></a>

