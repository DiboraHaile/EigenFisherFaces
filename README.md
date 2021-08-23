# Face Recognition with Eigen and Fisher Face Algorithms

Face recognition by using Eigen and Fisher Face Algorithms.
The first Recognition algorithm implemented is Eigen Face. We collected the dataset and
preprocessed the data we collected. The pictures were cropped and resized appropriately so
they can be fed to the algorithm.

1. Eigen Face Algorithm
## Generated Mean image from our dataset
![alt text](https://github.com/DiboraHaile/EigenFisherFaces/blob/main/images/mean.jpg?raw=true)

After finding the reduced eigenvectors, we create the projection of our image space. To classify
a new image we compute the difference between the projection of the new image with the
projection of each image in the database. We then select the one with the minimum distance
and find out the class it belongs to. The accuracy of this model is 87.

![alt text](https://github.com/DiboraHaile/EigenFisherFaces/blob/main/images/eigenfaceresult.png?raw=true)

2. Fisher Face Algorithm
After calculating the mean face from the dataset and then the mean of each class. We then
calculated PCA since the number of images in the database is greater than the dimension of the
images. We used the PCA implementation used for eigenfaces to reduce the dimensions. We
found the eigenvectors and used them to get the weight of the images. We then applied LDA on
these weights to get the fisher faces.

![alt text](https://github.com/DiboraHaile/EigenFisherFaces/blob/main/images/fisherfaces.png?raw=true)

Then during recognition, we compared the weight of the image to the weights of the classes and
found the class with the minimum distance using KNN. we selected the optimum numbers of K
based on the accuracy it produced and that value is 3.
The output of our models are displayed as the following, we were able to get an accuracy of
70%.

![alt text](https://github.com/DiboraHaile/EigenFisherFaces/blob/main/images/fisherfaceresults.png?raw=true)









