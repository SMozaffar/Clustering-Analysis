# K-Means vs. Spectral Clustering

Clustering, a type of unsupervised learning, is used to capture the structure, grouping, and underlying processes immanent in a dataset. The goal of clustering is to separate the data into distinct groups in such a way that data points in the same groups are more similar to each other than data points in other groups. Here, we explore two different clustering algorithms, K-means and spectral clustering, to get an insight into how they work and compare their performance on data in a two-dimensional space. 


### The Data

The dataset contains 1125 rows and 3 columns: 'Field', 'x', and 'y'. Each row represents a data point, and the columns represent the index and x-y coordinate locations of each data point, respectively. The first ten columns of the dataset and a scatterplot of the data are shown below

<div align="center">

|FIELD1|x                  |y                   |
|------|-------------------|--------------------|
|1     |-1.06519785476848  |2.41602231329307    |
|2     |0.20061166305095   |0.0508693247102201  |
|3     |-2.15951012307778  |-0.225542888045311  |
|4     |-0.643773137591779 |2.18496798584238    |
|5     |-0.975246698129922 |-0.702547463122755  |
|6     |-0.911281818989664 |0.637968627735972   |
|7     |0.321858583018184  |-1.01905076019466   |
|8     |-1.08197453571483  |2.64709240570664    |
|9     |1.22096595587209   |2.0513566522859     |
|10    |-2.30543425306678  |1.45974390394986    |



![](images/1.png)

</div>


### K-means Clustering

Given *n* data points, the objective is to divide them into *K* groups such that:
    - data points in a group are very similar to eachother
    - data points in two different groups are less similar

But how do we define similarity? K-means uses the Euclidean distance between two points as the default distance metric for clustering. 

The **K-means loss** is given by:
$$ \sum_{k}\sum_{i\in  C_{k}}\left|\left|x_i-\mu _k \right| \right|^2$$
