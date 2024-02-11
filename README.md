# Vento Cycle Path Charging Infrastructure
relized by Calvi Mirko
Fondations of Operations Research, 2024, Politecnico of Milan

## introducttion 
Consider a long linear cycle path as Vento, or the Danube cycle path. The cycle path usually runs along the banks of a river with scarce tourist interest. However, from the main course of the cycle path, it is possible to reach places of tourist interest by making small detours.

The rapid growth of e-bike ridership is proposing the problem of deploying a suitable charging infrastructure. The charging stations should be placed in strategic positions to guarantee coverage of the entire cycle path. However, since the charging operations require a non-negligible amount of time, the charging stations should be positioned in places where alternative activities could be carried out, such as restaurants, museums, swimming pools, or other amenities. Moreover, the presence of a charging station could also induce e-cyclists to discover new places and generate positive externalities.

## goal
Minimize the total lenght of the cycle path and, given a maximum budget to spend, minimize the maximum distance between charging stations.
It is strongly suggested to continue the reading from the .ipynb file.

## key points

### Touristic city geographical locations:
![locations](https://github.com/MirkoCalvi/Vento_bicycleLane_optimization_problem/assets/118633160/5f627a03-5078-4374-8c04-723346d02eeb)

### shortest path touching all the cities:
To compute the shortest path I used a modified TSP (The Salesman Problem) algorithm. In the code you can see a method to dedect and avoid loops in the graph. 
TSP algorithm reveals to be extremelly effective. When the graph is too dense TSP is not efficent, so I suggest to do some data cleaning, like only taking the 5 closest cities an don't compute the distance for each possible node.

![shortest_path](https://github.com/MirkoCalvi/Vento_bicycleLane_optimization_problem/assets/118633160/161509d4-0e0f-4787-9d74-9d034b7b2ddd)
![clean shortest_path](https://github.com/MirkoCalvi/Vento_bicycleLane_optimization_problem/assets/118633160/dbf4d174-816c-4e20-a462-74d26bd2a071)

### chargin stations positioning
#### 10k budget

![10k budget](https://github.com/MirkoCalvi/Vento_bicycleLane_optimization_problem/assets/118633160/529d416f-548d-4ce7-a5c8-29389a09a374)

#### 30k budget

![image](https://github.com/MirkoCalvi/Vento_bicycleLane_optimization_problem/assets/118633160/c7aaed08-8820-4c55-bf56-37dacb1e568a)

#### 40K budget

![image](https://github.com/MirkoCalvi/Vento_bicycleLane_optimization_problem/assets/118633160/54f5605a-6d25-4e62-8c80-d250ebdc39d0)

other budgets are present in the .ipynb file
As you can see there is a threshold at 16011.18979 [m] (0->43), so using a budget over 29892 euros wont improve the minimixed maximum distance between stations.



