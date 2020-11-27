PROCEDURE:

1. The PCA calculation is as same as in assignment-3.
2. The eigensignatures from the PCA are taken as training set input to ANN.
3. n - no of nodes for hidden layer (n=360).
4. c - no of nodes for outer layer (no of classes).
5. Random weights are assigned for both hidden and outer layer in range -0.5 to 0.5.
6. Random threshold values are assigned for both hidden and outer layer in range 0.1 to 1.0 .
7. Learing rate is choosen randomly in range 0.1 to 1.0 .
8. Till the cost function is less than 0.001 the neural network layers are trained as:
9. Cost function initialized to zero.
10. For every image,
	a. The actual output of both layer nodes calculated using sigmond func(1/(1-exp(-x))).
	b. The cost/loss is calculated using the outer layer actual output and expected output.
	c. The cost is added to the cost function.
	d. The Error is calculated for the outer layer and using that the error for hidden layer is calculated.
	e. The weights and threshold values are modifies based on the errors.
11. step-9 and step-10 are repeated till the cost function is less than 0.001, but for faster execution 
	we have limited the no of  epochs.
12. For every 25 epochs, the accuracy is calculated and stored.
13. Finally, The accuracy vs no of epochs   and  cost function vs no of epochs are plotted.


Observations:

From the plots, it is clear that:
a. Accuracy increases with increase in no. of epochs.
b. Cost function(loss) dereases with increase in no. of epochs.
c. Accuracy increases with decrease in cost function.

Training with ANN takes more amount of time than with PCA.

	