
#---Maintenance scheduling---#

Procedure:

1. Given data(capacity, intevals..) is initialized.
2. initial population is generated randomly based on required size(N).
3. No. of Generations to be evolved is considered as the termination criteria.
4. For each generation, 
	a. Fitness values of each chromosome is calculated.
		Here, Fitness value is taken as the minimum of net reserve of all the intervals.
	b. Fitness ratios of each chromosome is calculated.
	c. New Generation is initialized,
	d. untill the new generation size equals current generation:
		- Using Roulette wheel selection based on the fitness ratios two parents were selected.
		- Based on the crossover probability two off-springs are produced on crossover of parent chromosomes.
		- Based on the mutation rate the two off-springs undergoes mutation.
		- These off-springs were added to the new generation.
		- The best fitness value, avg fitness value and valid Schedulings were stored.
5. The best fitness, avg fitness values were plotted against generations for 
	N = 20, generations = 100, crossover_prob = 0.7, mutation_rate = 0.001	
	N = 100, generations = 100, crossover_prob = 0.7, mutation_rate = 0.001	
	N = 100, generations = 100, crossover_prob = 0.7, mutation_rate = 0.01	
	here,
		N                -> population size
		generations      -> no. of generations
		crossover_prob   -> crossover probability 
		mutation_rate    -> mutation probability

6. Some valid Schedulings were printed.

observations:

- With low initial population the best fitness values are less frequent when compared to the high initial population.
- With increase in mutation rate the the fluctuation in average fitness values is very high and increase slowly.

=======================================================================================================================================

#---N-queen (8-queen)---#

Procedure:

1. The initial population is taken as permutations of 1 to 8, since we know the valid configuration will be a permutation of 1-8.
2. This initial population requires modified crossover and mutation algorithms to keep the chromosomes as permutations of 1-8.
3. No. of Generations to be evolved is considered as the termination criteria.
4. For each generation, 
	a. Fitness values of each chromosome is calculated.
		Here, Fitness value is taken as the no. of non-attacking pairs of queens.
	b. Fitness ratios of each chromosome is calculated.
	c. New Generation is initialized,
	d. untill the new generation size equals current generation:
		- Using Roulette wheel selection based on the fitness ratios two parents were selected.
		- Based on the crossover probability two off-springs are produced on crossover of parent chromosomes.
			Modified crossover funtion:
				+ Generate two random points between 1-8.
				+ genes between these points of parent1 are carried to child1 in the same positions.
				+ The genes of parent2 which are not present is child1 were carried to child1 in same order.
				+ vice-versa for child2.
		- Based on the mutation rate the two off-springs undergoes mutation.
			Modified mutation funtion:
				+ Generate two random points between 1-8.
				+ These two genes are interchanged.
		- These off-springs were added to the new generation.
		- The best fitness value, avg fitness value and valid Configurations were stored.
5. The best fitness, avg fitness values were plotted against generations for 
	N = 100, generations = 100, crossover_prob = 0.5-0.7, mutation_rate = 0.001	
	N = 100, generations = 200, crossover_prob = 0.5-0.7, mutation_rate = 0.001	
	N = 500, generations = 100, crossover_prob = 0.5-0.7, mutation_rate = 0.001	
	N = 1000, generations = 100, crossover_prob = 0.5-0.7, mutation_rate = 0.001	
	here,
		N                -> population size
		generations      -> no. of generations
		crossover_prob   -> crossover probability 
		mutation_rate    -> mutation probability

6. Some valid Configurations were printed.



Observations:

- With general crossover and mutation funtions and initial population, The valid configurations were obtained very slowly but the 
  average fitness is high and close to best fitness value.
- With modified crossover and mutation funtions and initial population, The valid configurations were obtained very quicly but the 
  average fitness is low when compared to best fitness value.

- With large initial population the best fitness values are more frequent when compared to the low initial population.