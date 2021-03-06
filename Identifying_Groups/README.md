
# Identifying Groups

## Introduction

The objective of finding groups within data is to find the right balance between similarities and differences. 

On one hand we want to treat similar cases similarly to benefit from economies of scale and thus improve efficiency. On the other hand we want to address different cases in distinctive ways in order to improve action's effectiveness.
Thus, by grouping similar data together we are actually improving our business efficiency. 

In this repo, we will examine the practicality and performance of hierarchical cluster analysis (HCA) from a business perspective using real-world examples. 

**Disclaimer:** What follows is a reference to two courses from ESSEC Business School I found on coursera and  highly recommend checking them out:

1. [Foundations of Strategic Business Analytics](https://bit.ly/3vnJBZl) and
2. [Foundations of Marketing Analytics](https://bit.ly/32UFibO)
 

## HCA

To find the right balance between similarities and differences is exactly the same from a clustering perspective as to say maximizing the similarity within clusters and dissimilarity between clusters.

In statistics, similarity is often measured with the euclidean distance between samples. This can easily be done in Python with the `pdist()` function from `scipy.spatial.distance`. 

However, before computing the distance we need to make sure that our variables are comparable. Otherwise we need to standardize our data. this can be done using the function `scale()` from the `sklearn.preprocessing` module.

The clustering is then done by calling `linkage()` function from the module `scipy.cluster.hierarchy`. 
Pretty simple, isn't it?!


### Example 1: Stock Keeping Unit

The [first example](https://bit.ly/3vwxiKq) is concerned with improving the inventory of a company. 
Imagine that you're working as a supply and logistics manager, and want to organize your stock and delivery more efficiently. 

One possibility would be to analyze the sku along two dimensions:
* Average Daily Sales and
* Volatility

The volatility of something may be measured with  coefficient of variation (CV), also known as relative standard deviation (RSD). The CV is defined as the ratio of the standard deviation to the mean $C_v = \frac{\delta}{\mu}$.

### Example 2: Customer Segmentation using RFM


In today's competitive world, it is essential to understand customer behavior and categorize them based on their demographics and buying behavior. At the same time, the groups themselves should be clearly differentiated from each other in terms of these characteristics and buying behavior according to the motto: "Customers are unique and sometimes similar".
The aim of the segmentation is to address and serve the respective individual customers in a way that best matches their specific group and characteristics. 

In this [example](https://bit.ly/3u6gQQA) we explore the concept of customer segmentation based on recency, frequency and monetary (RFM) model. The data set contains three variables: *customer_id, purchase_amount* and *date_of_purchase*, and 51k observations. 
