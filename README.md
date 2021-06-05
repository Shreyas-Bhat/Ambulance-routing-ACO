# Ambulance-routing-ACO

### Problem Statement
* The hospital routing problem is a contextual variation of the traveling salesman problem
* "What is the optimal set of routes for a fleet of vehicles to traverse to deliver to a given set of customers?". 
### Solution Model
* I have adopted a multi ant colony system - vehicle routing problem with time windows(MACS-VRPTW) for this problem which is based on the Ant Colony Optimization(ACO), the multiple ants, are organized in a manner to solve a multi-objective problem which is - i) the minimization of the number of tours(or vehicles) and ii) minimization of total travel time. 
![image](https://user-images.githubusercontent.com/56354373/120896940-64b9bc80-c641-11eb-9e4a-a16ac392ff3d.png)

### ACO Pseudo-Code
```
Best Tour := NIL

repeat 

	Randomly place M ants on N cities 
	each ant constructs a tour in a greedy stochastic manner 
	update best_tour
	Each ant deposits pheromone on tour edges*
Until a termination criteria is met
return best_tour

*In the real world, ant keeps on depositing pheromone 
```
### ACS-VEI Procedure
```
/* cycle */
/* compute number of times a patient has visited*/
/* initialize pheromone and data structure and initialize solution with N hospitals using nearest neighbour heuristic*/
for each ant k:
     construct a solution 𝜙k  
     insert(INj)
     new_ant()
     /*update for best solution if it is improved*/
if visited_patients(𝜙k) > visited_patients(𝜙ACS-VEI)
    𝜙ACS-VEI := 𝜙k
     /* if feasible, send for VRPTW */
/* perform update on both 𝜙k and 𝜙ACS-VEI   */
τij = (1-ρ)τij  +ρ/Jk
τij = (1-ρ)τij  +ρ/JACS-VEI
until a stopping condition is met 
```
### [References](https://github.com/Shreyas-Bhat/Ambulance-routing-ACO/blob/master/SOP%20report.pdf)
