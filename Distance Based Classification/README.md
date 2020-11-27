Procedure:

1. Initially the data is loaded using pandas library from the file iris.csv.
2. Then the features and clsses are extracted to X and Y variables and the feature data is scaled/normalized.
	Different features vs feature graphs are plotted and classification of thee samples is observed.
3. The data is splitted into 80% of train_set and 20% of test_set.
4. The averages for each class data are calculated (centroids) using the train_set.
5. Then for each distance classifier,
	a. calculated the distance between the three class centrioids.
	b. minimum distance class is identified and if wrongly predicted the misclassification rate is increased.
	c. The distance is added for error sum and its square is added to square error sum for different classifiers.
6. based on the misclassification data , Classifier Vs Misclassification error rates is plotted.
7. The mean error and mean squared error and mean absolute error are calculated and plotted.

Observations:

From the Classifier Vs Misclassification error rates plot:
	it is clear that, cosine distance classifier gives the least misclassification rate
	and the misclassification rates are always very less.
From the different mean errors VS Distance classifiers plot:
	it is identified that mahalanobis distance classifier errors are more than other classifiers
	and cosine distance classifier errors are very less.
