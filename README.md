# Column generation for cutting stock problem
This is a example of solving 1-D cutting stock problem by column generation.


There are two class: MasterProblem and SlaveProblem obtained by Dantzig-Wolfe decomposition.

Master problem has a formulation like:
<img src="https://render.githubusercontent.com/render/math?math=e^{i \pi} = -1">
        min \;z = \sum_{j=1}^{n} x_{j} \\
        \sum_{j=1}^{n} a_{ijxj} \ge d_{i} \qquad i = 1, ...,m \\
        x_{j} \ge 0 \qquad i = 1, ...,n
