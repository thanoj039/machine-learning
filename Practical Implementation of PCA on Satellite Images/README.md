Procedure:

1.Intially, the input images were loaded

2.Then mean of each image is calculated

3. Then deviation matrices for both the classes were calculated.
		for(i,j,k)
		 	devMat[i][j][k]  =  input[i][j][k] - mean[k]
		i,j – image co-ords
		k- image number

4.Using deviation matrices co-variance matrices were calculated.
		covMat  =   (devMat’ * devMat) / n

5.Then eigenvalues and eigen vectors were calculated using “eig”

6.Transpose of each eigenvector is multiplied with input_data set to obtain the outputs 	One output image for each eigenvectors
