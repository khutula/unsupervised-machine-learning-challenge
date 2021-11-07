# GT Bootcamp Unsupervised Machine Learning Homework: Cryptocurrency Clusters

## Table of Contents
1. [Introduction](#introduction)
2. [Objectives](#objectives)
3. [Technologies & Tools](#technologies)
4. [Files & Links](#files)
5. [Analysis](#analysis)

<a name="introduction"></a>
### Introduction
In my new role on the Advisory Services Team of a financial consultancy, I have been tasked with assisting a client, a prominent investment bank, in determining if cryptocurrencies can be grouped together. I am expected to use raw data and process it using unsupervise machine learning methods.

<a name="objectives"></a>
### Objectives
Provide clustering recommendations to the client by:
* Reading in the dataset from the provided CSV
* Dropping unneeded columns
* Removing rows with null values or where mining is zero
* Converting categorical data to numeric dummy variables
* Standardizing the dataset
* Reducing dataset dimensions using PCA
* Reducing dataset dimensions using t-SNE
* Performing cluster analysis with k-Means
* Determining the optimal number of clusters based on an elbow curve
* Plotting the proposed clusters by color

<a name="technologies"></a>
### Technologies & Tools
This project uses: 
* Python
* Matplotlib Library
* SKLearn Library
* Pandas Library
* Jupyter Notebook

<a name="files"></a>
### Files & Links

* [Crypto Clusters Notebook](Crypto_Clusters.ipynb): notebook used for data preprocessing, dimensionality reduction, and cluster analysis
* [Raw Data](Resources/crypto_data.csv): raw data CSV file that contains the cryptocurrencies and their data 

<a name="analysis"></a>
### Analysis

#### PCA
Using PCA to reduce dimensions and preserve 90% of explained variance caused the number of columns to reduce from 98 to 74.

#### t-SNE
The t-SNE dimension reduction seems to give us three larger somewhat distinct clusters and one smaller but distinct cluster. It appears to be 4 clusters in total with a couple of outliers.

![image](https://user-images.githubusercontent.com/82410966/140663825-c8e22a2d-ad9a-4153-924d-6aca49bc8ae1.png)

#### Cluster Analysis & Recommendations
Based on my analysis and findings, I would recommend to the client that cryptocurrencies can be clustered together, and that the provided data suggests four clusters. One consideration to take into account is that there appears to be two significant outliers in the data. These could indicate either errors in the data or simply a significant difference between the other cryptocurrencies. I would recommend collecting more data to be certain that this model works, as we lost almost half the data during initial cleaning due to empty values or no trading being performed on that crypto.

![image](https://user-images.githubusercontent.com/82410966/140663839-1dac96b8-aa9b-4f4a-b125-40ce29ef8fc3.png)

![image](https://user-images.githubusercontent.com/82410966/140663847-2eec6802-6969-46c4-91be-f9be8732f7b4.png)


