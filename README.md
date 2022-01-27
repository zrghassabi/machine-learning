# machine-learning



"Machine Learning is the field of study that gives computers the ability to learn without being explicitly programmed." —Arthur Samuel, 1959


Supervised Learning: Classification, Regression (Polynomial, Ridge, LAsso, ElasticNet)

In Regression, Loss Function is MSE. In Classification, loss function is Cross-Entropy (Logarithmic or logistic Loss)

https://howsam.org/logistic-regression/

Unsupervised Learning: Clustering, Dimension reduction.


Terms: Gradient Desent, local minium, Learning Rate, 





-------------------------------------------------------------------------------------------------------------------------------------------------------------------------


Overview of Clustering : https://scikit-learn.org/stable/modules/clustering.html

a)Partitional Clustering: 
These techniques require the user to specify the number of clusters, indicated by the variable k. Many partitional clustering algorithms work through an iterative process to assign subsets of data points into k clusters. Two examples of partitional clustering algorithms are k-means and k-medoids.
These algorithms are both nondeterministic, meaning they could produce different results from two separate runs even if the runs were based on the same input.

strengths:

They work well when clusters have a spherical shape.
They’re scalable with respect to algorithm complexity.

weaknesses:

They’re not well suited for clusters with complex shapes and different sizes.
They break down when used with clusters of different densities.


b) Hierarchical Clustering (bottom-up approach:Agglomerative, top-down approach:Divisive)

*The number of clusters (k) is often predetermined by the user. Clusters are assigned by cutting the dendrogram at a specified depth that results in k groups of smaller dendrograms.

*Unlike many partitional clustering techniques, hierarchical clustering is a deterministic process, meaning cluster assignments won’t change when you run an algorithm twice on the same input data.

The strengths of hierarchical clustering methods:
They often reveal the finer details about the relationships between data objects.
They provide an interpretable dendrogram.

The weaknesses : 
They’re computationally expensive with respect to algorithm complexity.
They’re sensitive to noise and outliers.

c) Density-based 

The strengths:

They excel at identifying clusters of nonspherical shapes.
They’re resistant to outliers.

The weaknesses:

They aren’t well suited for clustering in high-dimensional spaces.
They have trouble identifying clusters of varying densities.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------

K-means :

  -The expectation step assigns each data point to its nearest centroid. 
  -the maximization step computes the mean of all the points for each cluster and sets the new centroid. 
  
Objective: to minimize SSE error or sum of squared distance of each poit to its closes centroid.

Notes: 
  -SSE will be used as a measure of clustering performance. 

  -the initialization of the centroids is an important step. 

  -After choosing a number of clusters and the initial centroids, the expectation-maximization step is repeated until the centroid positions reach convergence and are unchanged.
  
  -The random initialization step causes the k-means algorithm to be nondeterministic, meaning that cluster assignments will vary if you run the same algorithm twice on the same dataset. Researchers commonly run several initializations of the entire k-means algorithm and choose the cluster assignments from the initialization with the lowest SSE.




