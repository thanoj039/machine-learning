#---Multivariate linear regression for Categorical Data---#

Procedure:

1. Given data is loaded and columns with NaN values are dropped.
2. The data is divided into dependant features and (Independant feature)output (x and y).
3. The Categorical Data is encoded using the label encoder from the sklearn.preprocessing library.
4. The observations are splitted into train(80%) and test(20%) data.
5. Using SelectKbest and f-regression algorithm from sklearn.featureselection, the best five features were selected.
6. Based on these selected features the train and test data is taken.
7. Feature matrix X is constructed for train data by adding a column of 1's at 0 index to x.
8. co-efficient vector(beta) is calculated.
        
        beta = (X'*X)^(-1) * X' * y
        
9. The regression line is generated as    y = X @ beta. here, @ -> matrix multiplication.
10. The results of the test data are predicted.
11. The residual errors are plotted for train and test data.
       here, residual errors -> deviation of the actual result from the predicted result(regression line).
12. The Root mean square error is calculated and printed.       
13. Since, multivariate regression line cannot be plotted for many features,
   the predicted result (regression line) with respect to every feature with train and test data are plotted.
       Here, while plotting the regression for every feature, the pairs are sorted to make the regression line
       look neat(since, we are plotting the multivariate regression line with respect to each feature if not sorted
       it may look like scribbles).