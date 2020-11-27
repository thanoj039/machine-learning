Procedure:

Initially the input image is loaded.

----Applying k-means clustering-----

For every k in [2,5] ( taking k-means )

1.Initailize epsilon value(>=0), 
as epsilon value decreses -> clssification will be more accurate but also takes more time.

2.Initaializing k random centers ( values between 0 - 255) assing them to current means( M1 ).

3.For every pixel of input image assign the cluster(or mean(M1) ) index to which it is nearest.

4.Calculate next means(M2) from the classification( sum of cluster values/size of cluster ).

5.Checking if maximum of (M2 -M1) > epsilon, if greater then assign next means to current means(M1 = M2) and repeat from step - 3.

6.Different color is assigned to each pixel position based on the cluster it belong to and store it in out_image array.

7.The output image is formed from the out_image array and saved in the ouput folder.

8.The stored output images are displayed.