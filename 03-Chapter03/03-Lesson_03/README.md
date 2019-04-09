# ND025 - Supervised Learning - Lesson 05

#### Tags
* Author : AH Uyekita
* Title  :  _Hierarchical and Density-based Clustering_
* Date   : 09/04/2019
* Course : Data Scientist Nanodegree Program
    * COD    : ND025-br
    * **Instructor:** Jay Alammar

***

## K-means Considerations

The K-means limitations rely on the cluster circle shape, due to the concept has based on the distance to Centroid. Figure 1 shows an example when K-means has a good results.

![Figure 1 - Example for K-means.](01-img/nd025_c3_l03_01.png)

<em><center>Figure 1 - Example when K-means has good results.</center></em>

A similar problem is presented in Figure 2, but with a shape a bit streched. Clearly there are three cluster.

![Figure 2 - New dataset to be clustered.](01-img/nd025_c3_l03_02.png)

<em><center>Figure 2 - New dataset to be clustered.</center></em>

The results when apply it the K-means is presented in Figure 3. As you can see, the K-means did not divide the points as expected.

![Figure 3 - New dataset to be clustered.](01-img/nd025_c3_l03_03.png)

<em><center>Figure 3 - K-means results.</center></em>

This is the drawback of using K-means, generally the clusters should have circle or spherical shapes to be properly divided. Figure 4 shows an ilustrations with several datasets.

![Figure 4 - New dataset to be clustered.](01-img/nd025_c3_l03_04.png)

<em><center>Figure 4 - K-means outcome of several datasets.</center></em>

Founded on the problems presented to clusters different shapes of points, such as two crescent, two O rings, etc.. There are two other methods to cluster points as you can see in Figure 5.

![Figure 5 - New techniques to cluster.](01-img/nd025_c3_l03_05.png)

<em><center>Figure 5 - New techniques to cluster.</center></em>

## Hierarchical Clustering

This kind of cluster method has founded on the concept of each point is a cluster. For each step we should aggregate two points into one cluster. This is performed calculating the distance between clusters, the closest clusters should be merged into one.

Bear in mind, the way the distance is calculate determine the kind of the Hierarchical Clustering.

### Single-link Clustering

The Single-link Hierarchical Clustering aims to group the closest clusters into one. Figure 6 shows it.

![Figure 6 - Single-link Clustering.](01-img/nd025_c3_l03_06.png)

<em><center>Figure 6 - Single-link Clustering.</center></em>

As you can see, the Dendogram highest is the order to group the points. According to the "cut" of this dendogram you can determine the number of cluster you want.

#### Shortcoming

Due to the way used to group the points, this kind of Hierarchical clustering technique is prone to create clusters elongated as you can see in Figure 7.

![Figure 7 - Shortcoming of Single-link Hierarchical Clustering.](01-img/nd025_c3_l03_07.png)

<em><center>Figure 7 - Shortcoming of Single-link Hierarchical Clustering.</center></em>

Even more, sometimes the Single-link clustering creates cluster that covers all the points.

#### K-means Comparison

Figure 8 shows a comparison between K-means and Single-link.

![Figure 8 - K-means and Single-link comparison.](01-img/nd025_c3_l03_08.png)

<em><center>Figure 8 - K-means and Single-link comparison.</center></em>

The second, third, and sixth are the ones with better results. The first and the fourth falls into the shortcoming of one cluster eats up almost all points.

However, this problem could be overcame analysing the dendogram, as you can see in Figure 9.

![Figure 9 - Linkage Dendogram.](01-img/nd025_c3_l03_09.png)

<em><center>Figure 9 - Linkage Dendogram.</center></em>

In some cases, it is possible to see the clusters presence that it not reflected in the final. This is the case of the fourth example, where there are three cluster according to the level of the cut. The same happens in the fifth case.

Lastly, the Single-link Hierarchical Clustering **is not** part of Scikit Learn package.

### Complete Link Clustering

The complete-link is similar to the single-link, the difference rely on the way to calculate the distance. In this case, we uses the farthest distance points to use as parameter of grouping.

#### Shortcoming

Unfortunately, this kind of Hierarchical Clustering method also has a shortcoming. This is presented in Figure 10, the problem is the same of presented in Single-link where only one point is taking account to calculate the distânce.

![Figure 10 - Complete-link Shortcoming.](01-img/nd025_c3_l03_10.png)

<em><center>Figure 10 - Complete-link Shortcoming.</center></em>

### Average Link Clustering

Instead of using the closest or the farthest points, this method summarize the distances using the avarega.

![Figure 11 - Average Link.](01-img/nd025_c3_l03_11.png)

<em><center>Figure 11 - Average Link.</center></em>

### Ward's Method


![Figure 12 - Ward's Method.](01-img/nd025_c3_l03_12.png)

<em><center>Figure 12 - Ward's Method.</center></em>



## DBSCAN (Density-based Spatial Clustering of Applications with Noise)









.
