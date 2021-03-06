# Column generation for 1-D cutting stock problem
This is a example of solving one-dimensional cutting stock problem by column generation.


There are two class: MasterProblem and SlaveProblem obtained by Dantzig-Wolfe decomposition.

## Master problem
Has a formulation like:


<a href="https://www.codecogs.com/eqnedit.php?latex=min&space;\;z&space;=&space;\sum_{j=1}^{n}&space;x_{j}&space;\\&space;\sum_{j=1}^{n}&space;a_{ijxj}&space;\ge&space;d_{i}&space;\qquad&space;i&space;=&space;1,&space;...,m&space;\\&space;x_{j}&space;\ge&space;0&space;\qquad&space;i&space;=&space;1,&space;...,n" target="_blank"><img src="https://latex.codecogs.com/gif.latex?min&space;\;z&space;=&space;\sum_{j=1}^{n}&space;x_{j}&space;\\&space;\sum_{j=1}^{n}&space;a_{ijxj}&space;\ge&space;d_{i}&space;\qquad&space;i&space;=&space;1,&space;...,m&space;\\&space;x_{j}&space;\ge&space;0&space;\qquad&space;i&space;=&space;1,&space;...,n" title="min \;z = \sum_{j=1}^{n} x_{j} \\ \sum_{j=1}^{n} a_{ijxj} \ge d_{i} \qquad i = 1, ...,m \\ x_{j} \ge 0 \qquad i = 1, ...,n" /></a>

## Slave problem:
Has a formulation like:


<a href="https://www.codecogs.com/eqnedit.php?latex=max&space;\sum_{i=1}^{m}&space;u^*_{i}&space;q_{i}&space;\\&space;\sum_{i=1}^{m}&space;l_{i}&space;q_{i}&space;\le&space;L&space;\\&space;u_{i}&space;\in&space;\mathbb{Z}&space;\qquad&space;i&space;=&space;1,&space;...,m&space;\\&space;u_{i}&space;\ge&space;0&space;\qquad&space;i&space;=&space;1,&space;...,m" target="_blank"><img src="https://latex.codecogs.com/gif.latex?max&space;\sum_{i=1}^{m}&space;u^*_{i}&space;q_{i}&space;\\&space;\sum_{i=1}^{m}&space;l_{i}&space;q_{i}&space;\le&space;L&space;\\&space;u_{i}&space;\in&space;\mathbb{Z}&space;\qquad&space;i&space;=&space;1,&space;...,m&space;\\&space;u_{i}&space;\ge&space;0&space;\qquad&space;i&space;=&space;1,&space;...,m" title="max \sum_{i=1}^{m} u^*_{i} q_{i} \\ \sum_{i=1}^{m} l_{i} q_{i} \le L \\ u_{i} \in \mathbb{Z} \qquad i = 1, ...,m \\ u_{i} \ge 0 \qquad i = 1, ...,m" /></a>


## Instance
In the file instance.csv you can insert your items with structure like 
```
400
280,2
279,4
277,2
```
where :
- first element on top of file is the max_length of items in stock, which variable in code is called lunghezza_max_asse
- the othere elements are a couple of lenght and demands of i-th item.

## Options

### debug 
- ```True``` the solver run a little instance of defaul
- ```False``` the solver run a instance in ```instances.csv``` file

### mostraRisultati
- ```True``` show optimum of master problem and new pattern at each iteration
- ```False``` show only optimum of cutting stock problem with number of iteration


## Benchmarks

| nItems  | max_width (cm) | time (min) | iteration  | optimum |
| ------------- | ------------- | ------------- | ------------- | -------------|
| 4  | 110  |  0.2 s  |  7  | 47 |
| 23  | 50  | 1.4 s  | 37  |  23  |
| 38  | 150  | 2.9 s  | 61  |  31  |
| 177  | 400  | 1 m 7 s  | 396 |  236  |
| 230  | 400  | 1 m 8 s  | 556  |  382  |
| 313  | 500  | 6 m 20 s  | 1092  |  330  |
| 496  | 1000  | 18 m 2 s  | 2660  |  504  |
