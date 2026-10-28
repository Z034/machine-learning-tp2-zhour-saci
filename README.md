# LAB 2 : Standrdized PCA

**Student** : SACI Zhour - G2

## Part A :
We build PCA by hand: standardize the grades, compute the covariance matrix, take its eigenvalues and eigenvectors, keep the top 2, and project the students onto them.
 
## Part B :
We get the same result in a few lines using `StandardScaler` and Scikit-learn's `PCA`.
 
## Part C :
We compare both results, which match except for a possible sign flip of a component, and check how much variance PC1 and PC2 keep.

## Interpretation of the findings
- Both implementations give the same eigenvalues, explained variance and coordinates, up to a possible sign flip.
- PC1 is a “general performance” axis if all its loadings have the same sign (check W[:, 0]), separating strong from weak students.
- PC2 captures the small remaining differences between subjects. Look at the signs in W[:, 1] to name it, rather than guessing.
- Two components are enough to represent the dataset.
 
### Summary:
PCA compresses the 4 strongly correlated grades into 2 new axes, with almost no information lost. The from-scratch and Scikit-learn versions agree, and sign differences are harmless since an eigenvector and its negative are both valid.
