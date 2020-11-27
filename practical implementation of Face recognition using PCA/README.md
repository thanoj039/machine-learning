Dataset used is AT&T face database from kaggle

Procedure:

1.Initially the dataset is loaded and it is splitted into training and testing set 60% and 40% respectively.
 i.e., for each face 6 images to train_set and 4 images to test_set

2.Mean image of the training set is calulated and substracted from all images to get the mean alligned faces.

3.Co-variance matrix is calculated from the mean alligned faces data
 i.e., cov_mat = ( mean_alligned-faces' * mean_alligned_faces )/112*92
 here, 112*92 -> images dimensions

4.Eigenvalues and eigenvectors are calculated using the eig library with co-variance matrix.

5.Based on the eigenvalues , for k in range 1 to 27 eigenvecotrs were choosen for the feature vector.

6.For each k value, 
	eigenfaces, signature and test_mean_alligned_data are calculated using the appropriate formulae,
	mean aligned faces are projected on eigen faces to get projected test faces,
	For each test face,
		the minimum of euclidean distance between eigenvectors and signature vectors is calculated,
		then, if the corresponding min_euclidean_dist_face mathches it's original face then correct predictions count is increased

7.Finally, for each k the respective accuracy (correct pred/total test input) is plotted.

8.From the plot, it is clear that from k=19 the accuracy is almost constant.

part-b -> finding imposters

9.Few faces doesn't belong to the train data were converted to grayscale images and stored.

10.These faces were placed at random location in test data and their locations were stored.

11.For k=19 the euclidean distances averages were calculated.

12.The average euclidean distances were sorted decreasingly.

13.let n-> the count of imposters added.

14.The first n largest average euclidean distances were predicted as imposters.

15.since the locations of imposters were stored, the accuracy of prediction of imposters is calculated and printed.