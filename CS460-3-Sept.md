# Class Assignment - 3 Sept, 2021
## Question
How do we determine $k$, the number of clusters, given that we already know $k$ means and DB SCAN?
## Answer
If the dataset is 2 or 3 dimensional, then visually creating a scatter plot of the data and taking a guess at how many clusters could be there could work.

But more generally, we could run $k$ means and DB SCAN on the data with an arbitrary $k$, and then for $k$ means, we could look at the results and calculate, for each $p$ in the dataset the distance $d(p,c)$, where $c$ is the centroid assigned to $p$, and add the distances up. Then we repeat this process for multiple values of $k$ and choose the $k$ for which the value of the distance sum, so to speak, is the least. This could work, perhaps.

And perhaps we can do something similar for DBSCAN, we run DB SCAN for different values of $k$ and $\epsilon$ and then see for which values of $(k,\epsilon)$, the number of outliers and the distance sum of the outliers from the nearest cluster is minimised.
