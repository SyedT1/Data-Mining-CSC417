# Assignment 4 Due Date: 06/08/2023
**Image data: MNIST data set**
| ![space-1.jpg](https://github.com/SyedT1/Data-Mining-CSC417/blob/main/Week%204/Screenshot%20from%202023-08-01%2018-04-49.png) | 
|:--:| 
| *MNIST Dataset* |
  1. Use google colab. Google colab has GPU so your program will be fast in google golab.
  
  2. We will in this assignment cluster images from MNIST (Mixed National Institute of Standards) database of handwritten digits. MNIST train data set containing N = 50000 grayscale images of size 28 × 28 as shown above. We will follow the steps specified below:
  
  3. After reading the train dataset, you will get a 784 × 50000 matrix digits and a 1 × 50000 matrix labels.
  
  4. We will not need labels for clustering. However, for external validation, we will use them. Each column of digits is a 28 × 28 grayscale image, stored as a vector of length 282 = 784 with elements between 0 and 1
  
  5. You are asked to apply the k-means algorithm to this set of N = 50000 vectors, with k = 10 groups, and starting from a random initial group assignment
  
  6. Calculate the quality of the final clusters using following criteria
     + Internal Validation
          + $$J=\frac{1}{N} \sum_{i=1}^N \min _{j=1, \ldots, k}\left\|x_i-z_j\right\|^2$$
          + Davies–Bouldin index
          + Dunn index
     + External Validation
          + Purity
          + Rand Index
  7. Plot the 3D plots for the randomly chosen 1000 data from the MNIST using the tsne. Use different colors for the points that are assigned to different clusters. Also plot the centroids in bigger markers.


**Text clustering: Reddit comments dataset**
1. Download Reddit comments: This data set (reddit_data.csv only) can be downloaded from [**here**](https://data.mendeley.com/datasets/85njyhj45m/1) and contains 39, 999 parent comments from May 2015 out of 5 subreddit pages. Since 1, 753 text entries are duplicates, only 38, 245 entries are used for further processing. The file includes the following information: 1. parent_id 2. text 3. topic 4. length 5. For this assignment, only the question and the topic information would be extracted. We use the text for clustering.
2. Now use following procedures to calculate feature vectors for the text associated with each reddit comments
   + Use the tokenizer to extract all words
   + Use stemming.
   + Normalize the words
   + Discard stop words.
   + Use Zipf’s law to discard most frequent and least frequent words
   + Build the final vocabulary/term list
   + Calculate TF matrix for all comments/documents. (You can’t use library functions)
   + Calculate normalized TF matrix (You can’t use library functions)
   + Calculate IDF for all terms (You can’t use library functions)
   + Calculate final weighted matrix for all documents. (You can’t use library functions)
   + Now use the rows as feature vectors for corresponding documents. Now add the category of the document in the first feature index. We will use it only to identify the text after clustering. We don’t use this information for clustering. We will use this information for external validation
   + Use K-mean clustering with the feature vectors to cluster the 38, 245 documents into 5 categories.
3. Calculate the quality of the final clusters using following criteria (You can’t use library functions)
     + Internal Validation
          + $$J=\frac{1}{N} \sum_{i=1}^N \min _{j=1, \ldots, k}\left\|x_i-z_j\right\|^2$$
          + Davies–Bouldin index
          + Dunn index
     + External Validation
          + Purity
          + Rand Index
