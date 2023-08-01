# Assignment 4 Due Date: 06/08/2023
**Image data: MNIST data set**
![](https://github.com/SyedT1/Data-Mining-CSC417/blob/main/Week%204/Screenshot%20from%202023-08-01%2018-04-49.png)
  1. Use google colab. Google colab has GPU so your program will be fast in google golab.
  
  2. We will in this assignment cluster images from MNIST (Mixed National Institute of Standards) database of handwritten digits. MNIST train data set containing N = 50000 grayscale images of size 28 × 28 as shown above. We will follow the steps specified below:
  
  3. After reading the train dataset, you will get a 784 × 50000 matrix digits and a 1 × 50000 matrix labels.
  
  4. We will not need labels for clustering. However, for external validation, we will use them. Each column of digits is a 28 × 28 grayscale image, stored as a vector of length 282 = 784 with elements between 0 and 1
  
  5. You are asked to apply the k-means algorithm to this set of N = 50000 vectors, with k = 10 groups, and starting from a random initial group assignment
  
  6. Calculate the quality of the final clusters using following criteria
