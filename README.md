# RecommendSystem
*This recommend system performs recommendations for movies using dataset of "movielens" 20M.*

:sparkles:  Author: Keke Lin




:octocat:

This repository contains:
1. The dataset of 20M movielens in data[data] {link.csv[link.csv], movie.csv[movie.csv], rating.csv[rating.csv]} and the dataset of 20M movielens in data[data] {links.csv[links.csv], movies.csv[movies.csv], ratings.csv[ratings.csv]}}after preprocessing to be used then.
2. The code Data_Processing.ipynb[Data_Processing.ipynb] to preprocess the dataset.
3. The code SVD_model.ipynb[SVD_model.ipynb] to perform the sparse SVD.
4. The code MF.ipynb[MF.ipynb] to perform the Matrix Factorization of sparse matrix.



## Table of Contents
- [Preprocess of Dataset](#preprocess-of-dataser)
- [SVD Model](#svd-model)
- [Matrix Factorization](#matrix-factorization)
- [Comparision of Models](#compareision-of-models)



 ## Preprocess of Dataset
 - The dataset, movielens, is downloaded from Kaggle[https://www.kaggle.com/grouplens/movielens-20m-dataset]. The datasets describe ratings and free-text tagging activities from MovieLens, a movie recommendation service. It contains 20000263 ratings and 465564 tag applications across 27278 movies. 
 - We preprocess the dataset by specifying the the age and occupations of uses, and then drop the duplicates of the dataframe.

## SVD Model

- To perform SVD Model we import libraries from Suprise package and use the cross_vadilate to compute the RMSE of the SVD algorithm.
- And the training performance are shown below.
!SVD[SVD.png]

## Matrix Factorization 
- The mothodology comes from the paper **"Matrix Factorization Techniques for Recommender Systems"**  published by IEEE Computer Society : [[1]](https://ieeexplore.ieee.org/document/5197422), [[2]](https://datajobs.com/data-science-repo/Recommender-Systems-[Netflix].pdf) 
- We define a MF class to specify the methods used in the paper. And peroform it for 50 iterations and 100 iterations.
![iteration50.png] ![iteration100.png]

## Comparision of Models
   
   |Model | RMSE| Trainig time(s) | 
   |:--------------:|:---------:|:---------:|
   |SVD    | 0.8737     | 42.79|
   |MF(50 times)    | 0.0002010    | 647.70|
   |MF(100 times)  | 0.0001998     | 1456.93|


