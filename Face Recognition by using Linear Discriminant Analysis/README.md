PROCEDURE:

1. The PCA calculation is as same as in assignment-3.
2. using those eigen faces as the projected faces in LDA, the following are calculated:
	means of each class,
	mean of total projeted faces.
3. Then class within scatter matrix is calculated based on the given equations using the class means and total means.
4. Then class between scatter matrix is calculated based on the given equations using the variances of the classes.
5. The criterion funtion is calculated using the within scatter matrix and between scatter matrix.
6. The test data is tested using both euclidean distance and manahabolis distance by both PCA  and LDA.
7. The accuracy results were plotted.

Observations:
using euclidean distance - LDA gives more accurate results than PCA.
using mahanabolis distance - LDA and PCA gives same results.
using euclidean distance - LDA gives more accurate results than all the combinations.
using mahanabolis distance - LDA and PCA gives same results and are better than using euclidean dist. with PCA.
Among all PCA with euclidean distance gives the less accurate results.
	