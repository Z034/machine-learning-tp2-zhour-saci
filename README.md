# LAB 2 : Standrdized PCA

** Student ** : SACI Zhour - G2

## Part A :
We build PCA by hand: standardize the grades, compute the covariance matrix, take its eigenvalues and eigenvectors, keep the top 2, and project the students onto them.
 
## Part B :
We get the same result in a few lines using `StandardScaler` and Scikit-learn's `PCA`.
 
## Part C :
We compare both results, which match except for a possible sign flip of a component, and check how much variance PC1 and PC2 keep.
 
### Summary:
PCA compresses the 4 strongly correlated grades into 2 new axes, with almost no information lost. The from-scratch and Scikit-learn versions agree, and sign differences are harmless since an eigenvector and its negative are both valid.
