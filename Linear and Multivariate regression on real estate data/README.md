
#---simple linear Regression---#

Procedure:

1. Given data is loaded and divided to features and output (x and y).
2. Regression line is generated for every feature seperately.
3. For each feature, 
	a. The observations are splitted into train(80%) and test(20%) data. 
	b. The co-efficients b0 and b1 are calculated for the regression line  h(x) = b0 + b1x .
        
        let, sig(x) -> sum of (x_i for 1<=i<=N)
        
        b1 =  (sig(x)*sig(y) - N*sig(xy)) / (sig(x)^2 - N*sig(x^2))
        b0 =  (sig(y) - b1*sig(x)) / N
        
	c. Using the regression line the test data output is predicted.
	d. The train data and test data actual vs predicted results(regression line) are plotted.
    e. The Root mean square errors are calculated and stored.
4. A bar graph is plotted for the Root mean square errors for every feature.


#---Multivariate linear regression---#

Procedure:

1. Given data is loaded and divided to features and output (x and y).
2. The observations are splitted into train(80%) and test(20%) data.
3. Feature matrix X is constructed for train data by adding a column of 1's at 0 index to x.
4. co-efficient vector(beta) is calculated.
        
        beta = (X'*X)^(-1) * X' * y
        
5. The regression line is generated as    y = X @ beta. here, @ -> matrix multiplication.
6. The results of the test data are predicted.
7. The residual errors are plotted for train and test data.
       here, residual errors -> deviation of the actual result from the predicted result(regression line).
8. The Root mean square error is calculated and printed.       
9. Since, multivariate regression line cannot be plotted for many features,
   the predicted result (regression line) with respect to every feature with train and test data are plotted.
       Here, while plotting the regression for every feature, the pairs are sorted to make the regression line
       look neat(since, we are plotting the multivariate regression line with respect to each feature if not sorted
       it may look like scribbles).