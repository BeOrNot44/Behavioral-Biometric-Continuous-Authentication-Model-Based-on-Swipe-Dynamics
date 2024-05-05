# Description

## Swipe Dynamics Methodology, Analysis, and Implementation 

In this Methodology, we explore the analysis, modeling, and implementation of swipe features for user authentication using machine learning techniques to obtain the optimal model. It comprises essential sections include: data analysis, feature visualization, swipe modeling, and implementation.

### 1. Data Analysis

The BB-MAS dataset contains approximately 1.7 million swipe data points from 117 individuals, collected over three months. Participants were given a phone with an app requiring them to type parts of a text and answer questions by swiping horizontally and vertically. Swipe and touch data were collected while reading and scrolling. In fact Prof. Jaafer AL-Saraireh preprocessed the data before. These features include start and end coordinates of swipes, distance, velocity quartiles, acceleration quartiles, pressure quartiles, area quartiles, swipe direction, tangent angle, and time taken for each event.

### 2. Feature Visualization

In the context of Swipe Feature Visualization, a heat map using Pearson Correlation technique was employed to analyze the relationship between features and determine their relevance. Heat maps visually depict linear relationships among features, aiding in identifying patterns and correlations. 

![Swipe Dynamics Features Heat Map](https://github.com/BeOrNot44/Continuous-Touch-Screen-Authentication-Model-Based-on-Swipe-Dynamics/blob/main/Images/Heat_Map.png?raw=true)

The relative importance of features was determined by the RF Classifier, with swipe type emerging as the most critical. Features with importance levels of 20% and above were included in the project.

![Feature Importance](https://github.com/BeOrNot44/Continuous-Touch-Screen-Authentication-Model-Based-on-Swipe-Dynamics/blob/main/Images/Feature_Importance.png?raw=true)

### 3. Swipe Modeling Methodology (Feature Selection and Classifier Selection)

The Swipe Modelling Methodology outlines the process of Feature Selection and Classifier Selection for the project. 

In terms of classifier selection, the results are based on the utilization of the complete set of 30 features. For evaluation, the Accuracy, Equal Error Rate, Recall, F1-Score, Precision used. Common algorithms which are used for multi-class classifications include k-Nearest Neighbors (KNN), Decision Trees (DT), Naive Bayes (NB), Random Forest (RF), Support Vector Machine (SVM) and Logistic Regression (LOG). The findings indicate that Random Forest (RF) achieved the highest accuracy with the lowest Equal Error Rate (EER) and nearly the fastest classification time. Although KNN and SVM also showed favorable results in accuracy and EER, they required significantly longer classification times compared to RF, exceeding 5 seconds.

![30 Feature Result](https://github.com/BeOrNot44/Continuous-Touch-Screen-Authentication-Model-Based-on-Swipe-Dynamics/blob/main/Images/30Feature_Result.png?raw=true)

Regarding Feature Selection methods, the emphasis was on enhancing accuracy and reducing EER, particularly for smartphone applications. Three Feature Selection method used, the 30-feature set was ranked, and the number of features was subsequently reduced:

1. Feature Importance (FI): 23 out of 30 features were selected.
2. Pearson Correlation (Corr): 26 out of 30 features were selected (Features with over 20% correlation were omitted).
3. Mutual Information (MI): 19 out of 30 features were selected.

These selected feature sets were used to train the models with the aim of obtaining the best-performing model based on the three algorithms mentioned.

The table below summarizes the performance of Random Forest (RF) and K-Nearest Neighbors (KNN) classifiers as both of them achieved more than 99% accuracy on a swipe model dataset, employing three feature selection methods: Feature Importance (FI), Persona Correlation (Cor), and Mutual Information (MI).

![RF_KNN_With_Selection](https://github.com/BeOrNot44/Continuous-Touch-Screen-Authentication-Model-Based-on-Swipe-Dynamics/blob/main/Images/RF_KNN_WithSelection.png?raw=true)

For RF, all feature selection methods achieved over 99% accuracy, with feature importance (FI) method yielding the highest accuracy of 99.7%. KNN, however, exhibited lower accuracy with all methods, indicating RF's superiority in this context. Finally, the ML results show that a subset of 23 features -selected using feature importance algorithm- was applied to an RF
classifier, achieving 99.7% accuracy rate in 0.56 second and 2.7% EER.

After training the RF with 23 features, a 100% accuracy was obtained in 0.56 seconds of time, with the features chosen having more than 20% importance. The selected features and their importance are shown in the list below.

![Feature Importance Details](https://github.com/BeOrNot44/Continuous-Touch-Screen-Authentication-Model-Based-on-Swipe-Dynamics/blob/main/Images/Feature_Importance_Details.png?raw=true)

### 4. Swipe Authentication Approach Model

Feature extraction after data pre-processing was carried out on the data and producing 30-features. Those features were used to obtain the best subset of features, which was 23 features in the end, by implementing the feature importance selection method. Finally, the data is loaded into the Swipe classification model, which is based on the RF classifier.

![Model Design](https://github.com/BeOrNot44/Continuous-Touch-Screen-Authentication-Model-Based-on-Swipe-Dynamics/blob/main/Images/Model_Design.png?raw=true)

*(Note: Model made by Mais Bataineh)*

### 5. Experiments Result using 23 Feature

All six algorithms were compared to determine their efficiency. The same dataset was used with a subset of 23 features. Figure below represents the RF confusion matrix.

![Confusion Matrix](https://github.com/BeOrNot44/Continuous-Touch-Screen-Authentication-Model-Based-on-Swipe-Dynamics/blob/main/Images/Confusion_Matrix.png?raw=true)

According to the confusion matrix, each instance in RF was correctly classified, with only a few exceptions misclassified. The table below summarizes the results of the classification algorithms.

![23 Feature Result](https://github.com/BeOrNot44/Continuous-Touch-Screen-Authentication-Model-Based-on-Swipe-Dynamics/blob/main/Images/23Feature_Result.png?raw=true)

### 6. Best Performance for Classifiers KNN, DT, RF with Swipe Dataset

The ideal parameters, such as the number of neighbors for KNN, the maximum depth for DT, and the number of estimators for RF, were fine-tuned to maximize accuracy and attain the best model.

![Best Performance](https://github.com/BeOrNot44/Continuous-Touch-Screen-Authentication-Model-Based-on-Swipe-Dynamics/blob/main/Images/BestPerformance.jpeg?raw=true)

### 7. Additions

![EER Comparison](https://github.com/BeOrNot44/Continuous-Touch-Screen-Authentication-Model-Based-on-Swipe-Dynamics/blob/main/Images/EER_compartion.png?raw=true)
![Accuracy Comparison](https://github.com/BeOrNot44/Continuous-Touch-Screen-Authentication-Model-Based-on-Swipe-Dynamics/blob/main/Images/Accu_Compartion.png?raw=true)

#### Have a Good Day 😊
