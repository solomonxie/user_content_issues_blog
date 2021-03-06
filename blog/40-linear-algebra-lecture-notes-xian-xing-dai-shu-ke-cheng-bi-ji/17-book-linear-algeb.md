# Book: Linear Algebra for Machine Learning (Jason Brownlee)

> "Linear algebra is a pillar of machine learning." - Jason

Check [THIS LINK](https://www.scribd.com/document/371769141/Jason-Brownlee-Basics-for-Linear-Algebra-for-Machine-Learning-Discover-the-Mathematical-Language-of-Data-in-Python-2018) for reading book: _Jason-Brownlee-Basics-for-Linear-Algebra-for-Machine-Learning-Discover-the-Mathematical-Language-of-Data-in-Python-2018_

## Linear Algebra Is Important in Machine Learning

![image](https://user-images.githubusercontent.com/14041622/39855453-94745df2-545e-11e8-9ad4-ae3e749999c1.png)

## Study Linear Algebra Too Early

![image](https://user-images.githubusercontent.com/14041622/39855632-3c40d024-545f-11e8-8d20-7671aa6b5f78.png)

## Study Too Much Linear Algebra

![image](https://user-images.githubusercontent.com/14041622/39855715-95d255ea-545f-11e8-9822-1182eb42d31a.png)

## Study Linear Algebra Wrong

![image](https://user-images.githubusercontent.com/14041622/39855774-db81e4f2-545f-11e8-8986-bad7de8ed936.png)

## A Bette Way To Study Linear Algebra

![image](https://user-images.githubusercontent.com/14041622/39855844-1e4bb84e-5460-11e8-9d30-edf5c45a4a74.png)

## What will be learnt in this book

- Vector norms
- Matrix multiplication
- Matrix properties
- Tensor & its operations
- Matrix factorization: `Eigendecomposition` & `Singular Value Decomposition (SVD)`
- `Principal Component Analysis (PCA)`
- `Linear Least Squares Regression`

## Types of Matrices

1. Square Matrix
2. Symmetric Matrix
3. Triangular Matrix
4. Diagonal Matrix
5. Identity Matrix
6. Orthogonal Matrix

## Matrix Operations

1. Transpose
2. Inverse
3. Trace: Gives the sum of all of the diagonal entries of a matrix
4. Determinant
5. Rank: To estimate of the number of linearly independent rows or columns in a matrix. 

## Sparse Matrix

Matrices that contain mostly zero values are called `sparse`, distinct from matrices where most of the values are non-zero, called `dense`. 

> Very large matrices require a lot of memory, and some very large matrices that we wish to work
with are sparse.
In practice, most large matrices are sparse — almost all entries are zeros.

## Matrix Decompositions

![image](https://user-images.githubusercontent.com/14041622/39865245-cb298546-547e-11e8-87b0-00dbd4609a26.png)
![image](https://user-images.githubusercontent.com/14041622/39865262-db6c2f58-547e-11e8-84d0-0a6fa3eb13cd.png)


Most common types of matrix decomposition:
- LU Decomposition
- QR Decomposition
- Cholesky Decomposition

### LU Decomposition

> The factors L and U are triangular matrices. The factorization that comes from `elimination`.

#### LUP Decomposition

![image](https://user-images.githubusercontent.com/14041622/39875803-3156534c-54a4-11e8-92ea-01c80f5ccdc1.png)


### QR Decomposition

![image](https://user-images.githubusercontent.com/14041622/39875972-a3bbd970-54a4-11e8-8916-a07b86443380.png)
![image](https://user-images.githubusercontent.com/14041622/39875990-b05e2f3e-54a4-11e8-9058-e29f5472f96c.png)
![image](https://user-images.githubusercontent.com/14041622/39876123-02fb0244-54a5-11e8-9ad7-30934e38f0b6.png)

### Cholesky Decomposition

The Cholesky decomposition is for square symmetric matrices where all values are greater than zero, so-called positive deﬁnite matrices. 
![image](https://user-images.githubusercontent.com/14041622/39876349-83aa0c46-54a5-11e8-82b1-7fc2b216038e.png)
Where L is the Lower triangular matrix, and Lᵀ is its transpose.
Or
![image](https://user-images.githubusercontent.com/14041622/39876376-92226d9a-54a5-11e8-82ef-765289477d98.png)
Where U is the Upper Triangular matrix, and Uᵀ is its tranpose.


## Eigendecomposition

> Eigendecomposition of a matrix is a type of decomposition that involves decomposing a square
matrix into a set of eigenvectors and eigenvalues.
One of the most widely used kinds of matrix decomposition is called eigendecomposition, in which we decompose a matrix into a set of eigenvectors and eigenvalues.

![image](https://user-images.githubusercontent.com/14041622/39876647-4f265c9e-54a6-11e8-8403-f0e113d990ae.png)
![image](https://user-images.githubusercontent.com/14041622/39876931-212130de-54a7-11e8-9d40-cc1e0ae6bca6.png)
> Not all square matrices can be decomposed into eigenvectors and eigenvalues

The parent matrix can be shown to be a product of the eigenvectors and eigenvalues:
![image](https://user-images.githubusercontent.com/14041622/39877077-80d955e2-54a7-11e8-8ef6-88bd53ccfb63.png)
![image](https://user-images.githubusercontent.com/14041622/39877109-9d0310e6-54a7-11e8-9445-fcfb651aaf1e.png)

> Almost all vectors change direction, when they are multiplied by A. 
Certain exceptional vectors x are in the same direction as Ax. 
Those are the “eigenvectors”.

![image](https://user-images.githubusercontent.com/14041622/39877359-59650938-54a8-11e8-8b3b-35398d5a667a.png)
![image](https://user-images.githubusercontent.com/14041622/39877421-81430464-54a8-11e8-9f95-e86c1bdc98d4.png)


## Singular Value Decomposition (SVD)

> The Singular Value Decomposition is a highlight of linear algebra.

![image](https://user-images.githubusercontent.com/14041622/39877826-7e6a084a-54a9-11e8-8366-bea2b903026c.png)
![image](https://user-images.githubusercontent.com/14041622/39877951-c4149e1e-54a9-11e8-8401-050477bdbc50.png)
![image](https://user-images.githubusercontent.com/14041622/39878035-f65df424-54a9-11e8-86ee-3c5a6c37c796.png)

> The singular value decomposition (SVD) provides another way to factorize a matrix, into singular vectors and singular values. The SVD allows us to discover some of the same kind of information as the eigendecomposition. However, the SVD is more generally applicable.


## Pseudoinverse

![image](https://user-images.githubusercontent.com/14041622/39878330-a567ad0c-54aa-11e8-8a46-ace037f1fbe3.png)
![image](https://user-images.githubusercontent.com/14041622/39878352-b5abf588-54aa-11e8-99bd-aa1518c89339.png)


## Dimensionality Reduction

![image](https://user-images.githubusercontent.com/14041622/39878631-63b7f046-54ab-11e8-8a32-c247b7667164.png)

