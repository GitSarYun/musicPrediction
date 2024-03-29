# Music Prediction
### I see my life in terms of music - Albert Einstein



Using Billboard top 100 from 2000 to 2019 and spotify hit predictor dataset, predict which factors makes music as a hit. The model will predict whether the music can be a hit with the accuracy of 94%

<br>

![festival pircture](image/festival.png)

<br><br>

## Overview

1. Business Understanding
2. Data Understadning
3. Modeling
4. Evaluation
5. Conclusion
7. Repository

<br>

## 1. Business Understanding
"In the music market, superstars significantly dominate the market share, while predicting the top hit songs is notoriously difficult" according to Seon Tae Kin and Joo Hee Oh. (*Music Intelligence: Granular Data and Prediction of Top Ten Hit Songs*) <br>

In modern society, people often assume that famous star’s music is one of the most important factors of deciding whether music could be a hit. But there are many other factors of deciding whether music could be a hit such as tempo, energy, danceability, and number of weeks on chart (billboard). <br>
Knowing the important factor could help industry to predict which music could be a bigger hit which will help industry to make most advantageous entry point into the market.


<br>

## 2. Data Understadning

Two datas are used: <br>

1. Billboard top 100
Basic music list that considered as a hit
The original data were from 1990s to 2019. To increase the reliability of data, used data from 2000 to 2019
Because the data was too big, drop unnecessary information such as uri, writing credits, and lyrics.
Also, split the data in to two different groups: 2000 to 2009, 2010 to 2019.
https://www.kaggle.com/datasets/danield2255/data-on-songs-from-billboard-19992019 


2. Sportify Hit predictor Dataset
Data with extra features and components of the music
The dataset is from 1960 to 2019. To increase the reliability and combine with first data, only use data from 2000 to 2019
Drop unnecessary information and duplicate columns
https://www.kaggle.com/datasets/theoverman/the-spotify-hit-predictor-dataset?select=dataset-of-00s.csv

<br>

![image](https://user-images.githubusercontent.com/115171856/229910469-67afde62-b45a-4979-8a60-19ab8d8acadf.png)


<br>

## 3. Modeling

Three differnt model is used.
To find the basic relationship with each components of dataset, use multiple linear regression model.

As the baseline, use K-fold cross validation. Depends on the parameter, accuracy sometimes goes higher, but most of the time, accuracy stays under 25 percent

<br>

![k-fold](image/KNeighbor_2.png)

<br>

For the final model, used Decision Tree Classifier. Accuracy is 93.96 percent. With different parameter, accuracy can go to 89 percent. It is not overfitting, and clearly, it is not underfitting.

<br>

![download](https://user-images.githubusercontent.com/115171856/230223164-eb28719b-ae6d-46ca-8df3-b12f325a03d4.png)


<br>

#### All the steps for modeling are included in the actual file. To see every model at once, check MusicPrediction.ipynb. (https://github.com/GitSarYun/musicPrediction/blob/main/MusicPrediction.ipynb)  <br>

<br>

## 4. Evaluation

Baseline model, or the K-fold cross validation is extreme underfitting, and it cannot be used in reality. But on the other hand, the decision tree classifier's accuracy is a lot higher than K-fold cross validation, and it can be used in reality. <br>

<br>

![download](https://user-images.githubusercontent.com/115171856/230223290-15fc1a0b-a0c4-4680-a4e9-14b682a9637a.png)


<br>

But as it is shown in plot, it has an efficiency problem. There are too many components in the model that it is inefficient.

<br>

## 5. Conclusion

Because the decision tree classifier has an efficiency problem, it is recommended to create different types of group for data. Also, it is recommended to find the components of music that has is more essential to increase efficiency such as energy or danceability.


<br>

## 7. Repository

When coding, created dataInit file to initialize data. It clean and merged data with simple visualization. (https://github.com/GitSarYun/musicPrediction/blob/main/code/dataInit.ipynb) <br> <br>
Visual1.ipynb file has multiple linear regression model with simple visualization. (https://github.com/GitSarYun/musicPrediction/blob/main/code/visual1.ipynb) <br><br>
Visual2.ipynb has an K-fold with decision tree models. It also has some different parameters and different visualization which could be ignored. (https://github.com/GitSarYun/musicPrediction/blob/main/code/visual2.ipynb) <br><br>
Most coding is referencing to lectures from Flatiron AI Academy, not only from apprentiship, but also intensive section <br>

#### In sum, all codes that were actually used for the final modeling is combined in a single file called MusicPrediction.ipynb (https://github.com/GitSarYun/musicPrediction/blob/main/MusicPrediction.ipynb)  <br>

All the other coding files are inside of code file. (https://github.com/GitSarYun/musicPrediction/tree/main/code) <br>
All images are save in image file. (https://github.com/GitSarYun/musicPrediction/tree/main/image)

<br>

Presentation: <br>
powerpoint from presentation in pdf <br>
https://github.com/GitSarYun/musicPrediction/blob/main/Music%20Prediction.pdf
<br>


<br>

Data: <br>
data folder is https://github.com/GitSarYun/musicPrediction/tree/main/data

ziped data from billboard top 100 from 2000 to 2019: <br>
https://github.com/GitSarYun/musicPrediction/blob/main/data/billboardHot100_1999-2019.csv.zip <br>

Sportify Hit predictor Dataset: <br>
2000 to 2009: https://github.com/GitSarYun/musicPrediction/blob/main/data/dataset-of-00s.csv <br>
2010 to 2019: https://github.com/GitSarYun/musicPrediction/blob/main/data/dataset-of-10s.csv <br>

merged data from 2000 to 2009: https://github.com/GitSarYun/musicPrediction/blob/main/data/df_00.csv <br>
merged data from 2010 to 2019: https://github.com/GitSarYun/musicPrediction/blob/main/data/df_10.csv <br>

<br><br><br>

Sara Yun <br>
Flatiron Apprenticeship AI Academy Capstone
