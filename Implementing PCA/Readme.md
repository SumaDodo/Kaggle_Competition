This contains the implementation of PCA in Python. 

**Why PCA?**  
```
Too much of anything is not good for anything
```
- The answer to this question is primarily based on the fact that the data set at our disposal has vast amount of features associated with it and it is very important to understand and figure out which features are more important than others. This is an attempt to get closer to answering this question.

```
Expected Result:  
To project the feature space onto smaller subspace that represents the data well.

Noted Terms:
1. Pattern Classification Task
2. Multiple Discriminant Analysis
3. Linear Transformation Methods
```
**PCA vs MDA**  

|PCA|MDA|
|---|---|
|Projecting entire set of data onto a different subspace| determine a suitable subspace to distinguish between patterns that belong to different classes|
|trying to find the axes with maximum variances where the data is most spread|additionally maximizing the spread between classes|

**What we actually do with the data at hand?**
- We calculate the eigen vectors from the data and collect them in the scatter matrix.
- Each of the eigen vector is associated with the eigen value. We observe these eigen values. 
- Eigen values tell about the length or magnitude of the eigen vectors. 
- If the eigen values associated with the eigen vectors have relatively similar magnitude that indicates that they are in the same and good subspace.
- If some of the eigen values are much higher then we must keep the ones with the bigger eigen values as these contain more information about the dataset.
- If the eigen value is less or near to zero are less informative.

**Steps for PCA**  
1. Consider the dataset with d-dimensional samples.
2. Compute d-dimensional mean vector.
3. Compute the scatter matrix.
4. Compute Eigen vectors and corresponding eigen values.
5. sorting of the eigen values.
6. use this new eigen value matrix to transform the values to a new subspace.

**Note:** Eigen vectors and eigen values form the core of PCA. While eigen vectors define the directions of the new feature space, eigen values define their magnitude.  

---
**Results**  
1. Upon implementing PCA Analysis for the Hits dataset, we observe that all the four principal components have the information. Thus none of them can be dropped.  

![PCA_hits_dataset](https://github.com/SumaDodo/Kaggle_Competition/blob/master/Implementing%20PCA/PCA_hits_dataset.png)

**References:**  
1. [Implementing PCA](https://sebastianraschka.com/Articles/2014_pca_step_by_step.html)
