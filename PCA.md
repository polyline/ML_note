*This file is a simple note from Coursera Online Machine Learning Course by Prof. Andrew Ng*
*not completed*

Actually, this note should be completed after I finished the following study.
- ML courses about PCA
- Searching materials on the internet
- Related videoes on Youtube about PCA and SVD

And This note will cover
- What is PCA
- Why use or need PCA
- How does it work(simply)
- How to apply it in our work
- Could we reconstruct the original dataset?
- How to choose k?

Since it will invovle some concepts of Linear Algebra.

# What is PCA?
It was a method to find a low dimensional surface onto which to project the data so as to minimiza the squared projection error.

# Why use or need PCA?
Since we want to reduce the dimension of data in order to visualize it, for example, reduce a dataset for 3D to 2D.
Then we need to find out a 2D surface which has a minimun projection error to represent to dataset.
Also, when the algorithm runs too slowly or the data take over too many memory in the disk, we use PCA to compress features.

# How does it work
In the process, there are two main things we need to calculate or find.
- u1, u2, ..., uk(k is the number of reduced features)
- z1, z2, ..., zk

It means that after we found the reduced space, and then we need to get the unit vector of the new space.

We also need a way to convert all the old points to the reduced space, for examples, for **n-D** to **k-D**.

# How to choose k?
How do we decide k, which means how much do we want to compress our data to. 

Intuitively, we could start for k=1...to k=n, and find which gives a better result.(For each k, the compressed data should retain more than 99% of original data)

However, it would take too many time, so alternatively, we could use S matrix to help us compute it

      [U, S, V] = svd(sigma)

# When to use it?

Many people will automatically contain PCA as a necessary step in the algorithm, however, Prof. Andrew Ng didn't agree it.
He suggested us to train using the origin dataset and see the results.
If it the result is wrong, or it indeed used up too much disk space, or the algorithm runs way too low.
In this situation, we use PCA.

By the way, although PCA could reduce the number of features of data, it could not be regarded as a method to solve overfitting, since running PCA means abandoning some information from the dataset, and it could make you lose some precious information.

Pros and Cons?
