# Swipe Dynamics Methodology, Analysis and Implementation 
In this Methodology, we explore the analysis, modeling, and implementation of swipe features for user authentication using machine learning techniques to obtain the optimal model. It comprises four essential sections: data analysis, feature visualization, swipe modeling, and implementation.

# 1.1 data analysis
in here "The BB-MAS dataset contains approximately 1.7 million swipe data points from 117 individuals, collected over three months. Participants were given a phone with an app requiring them to type parts of a text and answer questions by swiping horizontally and vertically. Swipe and touch data were collected while reading and scrolling. In fact Prof. Jaafer AL-Saraireh preprocessed the data before. These features include start and end coordinates of swipes, distance, velocity quartiles, acceleration quartiles, pressure quartiles, area quartiles, swipe direction, tangent angle, and time taken for each event.

# 1.2 feature visualization

In the context of Swipe Feature Visualization, a heat map was employed to analyze the relationship between features and determine their relevance. Heat maps, visualizing data in a 2-dimensional format, help identify patterns, variances, and anomalies by displaying the density or intensity of variables. A correlation matrix, represented as a heat map grid, visually depicts the correlation coefficients between features. Strong dependencies are easily identified: positive correlation indicates a strong dependency, negative correlation an inverse one, and near-zero correlation a weak dependence.

In Figure below, the Swipe Dynamics Features Heat Map illustrates linear relationships among features, such as swipe coordinates, swipe type, and area correlations with velocity averages. Among the features, 7 exhibit negative correlation, 20 positive correlation, and 3 no correlation.

![Alt Text](https://github.com/BeOrNot44/Continuous-Touch-Screen-Authentication-Model-Based-on-Swipe-Dynamics/blob/main/Images/Heat_Map.png?raw=true)


Furthermore, Figure 1.2 demonstrates Swipe Features Importance, indicating the relative importance of features as determined by the RF Classifier. Swipe type emerges as the most important feature, with approximately 95% importance. Features with importance levels of 20% and above are included in the project.

![Alt Text](https://github.com/BeOrNot44/Continuous-Touch-Screen-Authentication-Model-Based-on-Swipe-Dynamics/blob/main/Images/Feature_Importance.png?raw=true)

# 1.3 swipe modeling Methodology (most important)

In the context of Swipe Features Importance illustrated in Figure 1.2, the Swipe Modelling Methodology outlines the process of feature selection and classifier selection for the project. 

In terms of classifier selection,in Table 1.1, the results are based on the utilization of the complete set of 30 features. For evaluation, the Accuracy, Equal Error Rate, Recall, F1-Score, Precision used. The findings indicate that Random Forest (RF) achieved the highest accuracy with the lowest Equal Error Rate (EER) and nearly the fastest classification time. Although KNN and SVM also showed favorable results in accuracy and EER, they required significantly longer classification times compared to RF, exceeding 5 seconds.

![Alt Text](https://github.com/BeOrNot44/Continuous-Touch-Screen-Authentication-Model-Based-on-Swipe-Dynamics/blob/main/Images/30Feature_Result.png?raw=true)

Regarding Feature Selection methods, the emphasis was on enhancing accuracy and reducing EER, particularly for smartphone applications. Three feature selection method used, the 30-feature set was ranked, and the number of features was subsequently reduced:

1.Feature Importance (FI): 23 out of 30 features were selected.
2.Pearson Correlation (Corr): 26 out of 30 features were retained.
3.Mutual Information (MI): 19 out of 30 features were identified as the most significant.

These selected feature sets were used to train the models with the aim of obtaining the best-performing model based on the three algorithms mentioned.

The table below summarizes the performance of Random Forest (RF) and K-Nearest Neighbors (KNN) classifiers as both of them achived more than 99% accuracy on a swipe model dataset, employing three feature selection methods: feature importance (FI), persona correlation (Cor), and mutual information (MI).

![Alt Text](https://github.com/BeOrNot44/Continuous-Touch-Screen-Authentication-Model-Based-on-Swipe-Dynamics/blob/main/Images/RF_KNN_WithSelection.png?raw=true)

For RF, all feature selection methods achieved over 99% accuracy, with feature importance (FI) method yielding the highest accuracy of 99.7%. KNN, however, exhibited lower accuracy with all methods, indicating RF's superiority in this context. Finally, the ML results show that a subset of 23 features -selected using feature importance algorithm- was applied to an RF
classifier, achieving (99.7%) accuracy rate in 0.56 second and 2.7% EER.

After training the RF with 23 features, a 100% accuracy was obtained in 0.56 seconds of time, with the features chosen having more than (20%)
importance. The selected features and their importance are shown in the list below.

![Alt Text](https://github.com/BeOrNot44/Continuous-Touch-Screen-Authentication-Model-Based-on-Swipe-Dynamics/blob/main/Images/Feature_Importance_Details.png?raw=true)

# 1.4 Swipe Authentication Approach Model

![Alt Text](https://github.com/BeOrNot44/Continuous-Touch-Screen-Authentication-Model-Based-on-Swipe-Dynamics/blob/main/Images/Model_Design.png?raw=true)

Feature extraction after data pre-processing was carried out on the data and
producing 30-features. Those features were used to obtain the best subset of features,
which was 23 features in the end, by implementing the feature importance selection
method. Finally, the data is loaded into the Swipe classification model, which is
based on the RF classifier.
note:model made by mais bataineh

# 1.5 Experiments Result using 23 feature

All six algorithms were compared to determine their efficiency. The same
dataset was used with a subset of 23 features. Figure below represents the RF
confusion matrix.

![Alt Text](https://github.com/BeOrNot44/Continuous-Touch-Screen-Authentication-Model-Based-on-Swipe-Dynamics/blob/main/Images/Confusion_Matrix.png?raw=true)

According to the confusion matrix, each instance in RF was correctly
classified, with only a few exceptions misclassified. The table below summarizes
the results of the classification algorithms.

![Alt Text](https://github.com/BeOrNot44/Continuous-Touch-Screen-Authentication-Model-Based-on-Swipe-Dynamics/blob/main/Images/23Feature_Result.png?raw=true)

# 1.6 Best performance for classifiers KNN, DT, RF with swipe dataset
![Alt Text](https://github.com/BeOrNot44/Continuous-Touch-Screen-Authentication-Model-Based-on-Swipe-Dynamics/blob/main/Images/BestPerformance.jpeg?raw=true)
# 1.7 Additions

![Alt Text](https://github.com/BeOrNot44/Continuous-Touch-Screen-Authentication-Model-Based-on-Swipe-Dynamics/blob/main/Images/EER_compartion.png?raw=true)
![Alt Text](https://github.com/BeOrNot44/Continuous-Touch-Screen-Authentication-Model-Based-on-Swipe-Dynamics/blob/main/Images/Accu_Compartion.png?raw=true)

# 1.8 Video:

![Project Image](https://youtu.be/bUh61Y1yY-w)
