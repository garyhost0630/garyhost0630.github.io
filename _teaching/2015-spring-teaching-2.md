---
title: "American Undergraduate Mathematical Contest in Modeling (MCM)"
collection: teaching
type: "Meritorious Winner"
permalink: /teaching/2015-spring-teaching-1
venue: "US"
date: 2023-05-09
location: "City, Country"
---

We are committed to solving [Problem C: Predicting Wordle Results](/mcm.pdf). For our full paper, you can click [here](/mcm_fullpaper.pdf).

## Abstract:

Wordle is a highly popular crossword puzzle on the **New York Times**. Through the five-letter words, the times players need to guess correctly and the number of players in hard mode, we analyze and predict the data of Wordle.

**For problem 1**, we preprocess the original data firstly, including correcting non-5-letter words, using **Cubic Spline Interpolation** and **Hermitian Interpolation** for abnormal value in reported results. Following the processed data, we apply the number of results in 2022 to the forecast model combining **ARIMA** and **GM(1,1)**, and find it present a descending trend. Then we predict that the number of reported results on March 1, 2023 will be between **[8067, 12406]**. Finally, we use **Ridge Regression** to explore the relationship between the percentage of people in hard mode and the attributes of word such as vowels, repeated letters, part of speech and word frequency. It shows that the regression coefficients corresponding to each attributes are less than 0.005, so we infer that hard mode percentage and word's attributes is **irrelevant**.

**For problem 2**, we use **One-hot**, **Bag of words**, **N-gram in NLP** respectively to encode words, applying which to **BP Neural Network** training to predict percentages of (1, 2, 3, 4, 5, 6, X). Then we find that the encoding method and word frequency will affect the accuracy of the model. The optimal number of iterations under the one-hot encoding method is 198, while under the N-gram is 545. Subsequently, for the given word EERIE, we predict that its percentages are **(0.84%, 5.50%, 10.63%, 18.35%, 28.48%, 26.13%, 10.05%)**. Finally, we test the accuracy of the model by calculating the average Euclidean Distance between the predicted and real value. The result shows that the average value of the Euclidean Distance of all words is , therefore the model is quite accurate.

**For problem 3**, we perform **Systematic Clustering** on 359 words, and determine the optimal number of clusters is 3 through the Elbow Rule, and then use K = 3 for **Kmeans** to classify words into easy, middle and hard types. Using XGBoost, Random Forest, and Adaboost as base classifiers, we establish an Ensemble Learning model of **Plurality Voting**, and the clustering labels are used to train the model. We analyze the attributes of different types and find that hard words have repeated letters, middle words start with vowels and easy words are prefixed with aspirated ch, th, etc. We use the model to determine the difficulty of EERIE and it shows that EERIE is of high difficulty. Finally, we make the sensitivity analysis on the ensemble learning model, and its classification accuracy is stable at around 85%, so the accuracy of the model is high.

**For problem 4**, We perform descriptive statistics on dataset and find that the number of players rose urgently in short term, and after March 2022, the number of players gradually decreased, while the percentage of hard mode increased by degree. At the same time, times of guesses obey the normal distribution, that is, most players need 3 to 5 tries to guess the word correctly.

**Keywords: Arima, Ridge Regression, NLP, BP Neural Network, Plurality Voting**

![](/mcm.jpg)
