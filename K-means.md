*This file is a simple note, if there is any fault, please contact me or edit it by git*

# What is K-means?
It's a clustering method which is popuplar and many people applied K-means algorithm in clustering problems.

# How does it work?
Simply, There are one initilization step and two main repeated steps.

Before starting explaning the steps, we should first know

- centroid, centroid points(Centroid means the center of each clustering group)
- clustering group

and some often used symbols

- m (m examples)
- K, k(the k-th clustering group, and the total number K clustering groups)
- n (n features)

## The initialization step
How do we initilizae K-means? We first need to assign value to each centroid point.

Instead of starting from zero or zero vector, we should ramdomly pick a point from m examples and assign it to our centroid 
point.

But it could still lead some problems, which we will talk about later.

## Find the closest cluster centroid to each example
Here are servels ways could be applied as the way of calculating distances.

In the class, we use Euclidean distance.

## Move centroid by averaging all the points in each group
After assigning each point to the closest centroid. We will have new groups.

And then we need to calculate the new centroid and update it.

After repeating this procedure, it's supposed to converge, and then we could get a great clustering result.

# Some Problems or Difficulties in K-Means
- local optima
- difficult to decide the number of clustering K
- the bigger K and the better result?

## Local Optima
In the initialization step, we ramdomly pick examples as the initialized centroid points.

However, sometimes it would not get a good result, intead, it would converge to local optima.

To solve this problem, we could do the initialization step many times(usually 50~1000 times), and choose the result with the minimun if J.

(J means the sum of all cost)

## Choose the Proper K
Even for human, sometimes it's hard to divide the data points into an exact number of clustering groups. Most of time, it could be ambiguous.

So, the best way to find out K is to do it by hand, and try different K and see which value could give a better result and the minimun cost.

As an optional choice, you could use Elbow Method to choose K, although sometimes it could contribute nothing.

Elbow methoud is a method by ploting a figure which x-axis is K and y-axis is J, and then find to elbow point as our K value.

Elbow point means literally, but in most cases, it still could be vague.

## The Bigger K and the Better Result?
It's hard to say, mathematically, the bigger K and the lower cost, unless there is a local optima problem.

But it depends on your purpose. You should pick the value K which meets your purpose.

