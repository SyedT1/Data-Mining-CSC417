Performing K Means clustering on **image** data and text data

[Image data:]{.underline} MNIST data
set![](./image1.png){width="1.8541666666666667in"
height="1.5416666666666667in"}

1.  Use google colab. Google colab has GPU so your program will be fast
    in google golab.

2.  We will in this assignment cluster images from MNIST (Mixed National
    Institute of Standards) database of handwritten digits. MNIST train
    data set containing *N* = 50000 grayscale images of size 28 *×* 28
    as shown above. We will follow the steps specified
    below:![](./image2.png)

3.  After reading the train dataset, you will get a 784 × 50000 matrix
    digits and a 1 × 50000 matrix labels. ![](./image3.png)

4.  We will not need labels for clustering. However, for external
    validation, we will use them. Each column of digits is a 28 × 28
    grayscale image, stored as a vector of length 28^2^ = 784 with
    elements between 0 and 1

5.  You are asked to apply the k-means algorithm to this set of N =
    50000 vectors, with k = 10 groups, and starting from a random
    initial group assignment![](./image4.png)

6.  Calculate the quality of the final clusters using following criteria

    a.  Internal Validation

> ![](./image5.png){width="1.7708333333333333in" height="0.5in"}

i.  

ii. Davies--Bouldin index

iii. Dunn index

```{=html}
<!-- -->
```
b.  External validation:

    i.  Purity

    ii. Rand index

```{=html}
<!-- -->
```
7.  Plot the 3D plots for the randomly chosen 1000 data from the MNIST
    using the tsne. Use different colors for the points that are
    assigned to different clusters. Also plot the centroids in bigger
    markers.

[Text clustering:]{.underline} Reddit comments dataset

a.  Download Reddit comments: This data set (reddit_data.csv only) can
    be downloaded from
    [[here]{.underline}](https://data.mendeley.com/datasets/85njyhj45m/1)
    and contains 39, 999 parent comments from May 2015 out of 5
    subreddit pages. Since 1, 753 text entries are duplicates, only 38,
    245 entries are used for further processing. The file includes the
    following information: 1. parent_id 2. text 3. topic 4. length 5.
    For this assignment, only the question and the topic information
    would be extracted. We use the text for clustering.

```{=html}
<!-- -->
```
1.  Now use following procedures to calculate feature vectors for the
    text associated with each reddit comments

    a.  Use the tokenizer to extract all words

    b.  Use stemming.

    c.  Normalize the words

    d.  Discard stop words.

    e.  Use Zipf's law to discard most frequent and least frequent words

    f.  Build the final vocabulary/term list

    g.  Calculate TF matrix for all comments/documents. **(You can't use
        library functions)**

    h.  Calculate normalized TF matrix **(You can't use library
        functions)**

    i.  Calculate IDF for all terms **(You can't use library
        functions)**

    j.  Calculate final weighted matrix for all documents. **(You can't
        use library functions)**

    k.  Now use the rows as feature vectors for corresponding documents.
        Now add the category of the document in the first feature index.
        We will use it only to identify the text after clustering. We
        don't use this information for clustering. We will use this
        information for external validation

    l.  Use K-mean clustering with the feature vectors to cluster the
        38, 245 documents into 5 categories.

2.  Calculate the quality of the final clusters using following criteria
    **(You can't use library functions)**

    a.  Internal Validation

> ![](./image5.png){width="1.7708333333333333in" height="0.5in"}

i.  

ii. Davies--Bouldin index

iii. Dunn index

```{=html}
<!-- -->
```
b.  External validation:

    i.  Purity

    ii. Rand index

```{=html}
<!-- -->
```
3.  Plot the 3D plots for the randomly chosen 1000 data from the Reddit
    comments using the tsne. Use different colors for the points that
    are assigned to different clusters. Also plot the centroids in
    bigger markers.
