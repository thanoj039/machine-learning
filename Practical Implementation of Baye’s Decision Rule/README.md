Procedure:

1.	The given image contains white space on all sides .
2.	Using MSpaint ( Grid and Scaling ), The co-ordinates of actual images were found.

			Co-ords obtained = (82, 30),  (594, 542)
			
3.	Using PIL library , The images were cropped.
4.	The cropped images were taken as input dataset.
5.	Random sample points were taken using MSpaint(Grid & Scaling) manually.
6.	River class 50 points were taken.
7.	Non-river class 100 points were taken.
8.	These were calculated:

		a.	Mean of River Class : T1 = [Mean1; Mean2; Mean3 ;Mean4]

		b.	Mean of non- River Class : T2 = [Mean1; Mean2; Mean3 ;Mean4]

              Here, mean[i] ->  mean of pixel values of the randomly selected points of i-th image
9.	Then deviation matrices for both the classes were calculated.

		for(i,j,k)

 			devMat[i][j][k]  =  input[i][j][k] - mean[k]

		i,j – image co-ords, 
		k- image number

10.	Using deviation matrices co-variance matrices were calculated.

        covMat  =   (devMat’ * devMat) / n

11.	Now for different ( Prior probabilities ) P1 and P2,
	Class conditional probability densities were calculated using the covariance matrices.
12.	Then Bayes theorem applied for input images,

		P1,P2 - > Prior probabilities

		p1,p2 - > class Conditional Densities

            		if((P1 * p1) >= (P2 * p2)):

                		output[i,j]=255

            		else:

                		output[i,j]=0

13.The output images are saved for different P1 and P2 values in the ouput folder.