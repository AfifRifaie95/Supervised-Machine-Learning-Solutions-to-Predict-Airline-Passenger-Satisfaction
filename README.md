# Supervised-Machine-Learning-Solutions-to-Predict-Airline-Passenger-Satisfaction
This report explores the application of machine learning techniques to predict airline
passenger satisfaction, identifying a crucial predictor for enhancing customer loyalty,
profitability and service quality. The study employs machine learning models, including K-
Nearest Neighbor (KNN), Random Forest and Gradient Boosting, applied to a dataset
containing passenger satisfaction metrics. A thorough exploratory data analysis (EDA), data
pre-processing steps, including one-hot, label encoding, and feature selection were
performed to ensure model accuracy. The algorithm was then optimized using
hyperparameter tuning methods, such as RandomizedSearchCV and GridSearchCV. The
results demonstrate that the tuned Gradient Boosting has achieved the highest accuracy of
95%, with features like online boarding, in-flight Wi-Fi service, passenger eco class and
personal type of travel being significant predictors of satisfaction. 

# Model Validation
Model                     Train  Accuracy    Test  Accuracy   Precision (Class 1)  Recall (Class 1)  F1 Score (Class 1)  ROC-AUC
Base K–Nearest Neighbor   94.3%               91.8%           94.4%                 86.3%             90.2%               96.0%
Tuned Random Forest       93.7%               93.1%           95.5%                 88.3%             91.8%               98.0%
Tuned Gradient Boosting   97.4%               95.0%           97.1%                 91.4%             94.2%               99.0%

                                      Table 1: Model Evaluation

Drawing from chosen algorithm including K – Nearest Neighbor, Random Forest and Gradient
Boosting, this analysis yields promising result with good performance. With all the selected
algorithms shows strong generalisation for its high accuracy and ROC-AUC score and the
output demonstrates there is no significant overfitting as the test metrics are close to the train
metrics. The tuned model KNN, Random Forest and gradient boosting, the model’s outputs
were validated using 5-folds cross-validation.
Tuned Gradient Boosting emerges as the top performer with test accuracy of 95.0% and
highest ROC-AUC score 99.0%. in predicting airline passenger satisfaction, followed closely by
Random Forest at 93.1%%. Interestingly, this study reveals that KNN as benchmark model
showing good performance with 91.8% with its base model. Hence, the base KNN model is
selected instead of the tuned model as the base model demonstrates better generalisation
with a balanced performance on both the train and test sets, avoiding the overfitting issues
observed with the tuned KNN model.  

According to highest performance technique, Gradient Boosting, Online Boarding as the most
critical feature, followed by Inflight Wi-Fi service, Class (Economy), Type of Travel (Personal
Travel), and Inflight entertainment. Other features like Departure Delay in Minutes, Food and
Drink, and Gender (Male) have minimal impact.

Model                 True Negativec(Class 0)  True Positives (Class 1)  False Positives (Class 0)  False Negatives (Class 1)
Base K–Neares Neighbor 11,228                   7,841                     469                        1,243
Tuned K–Nearest
Neighbor 11,276 7,987 421 1,097
Base Random
Forest 11,469 8,232 228 852
Tuned Random
Forest 11,320 8,020 377 1,064
Base Gradient
Boosting 11,243 8,085 454 999
Tuned Gradient
Boosting 11,451 8,299 246 785
Table 4: Confusion Matric Model Evaluation
The tuned Gradient Boosting confusion matrix also shows better precision and recall, it shows
enhanced performance and better generalization across all models. It achieved TN (11,451)
and TP (8,299) while reducing FP (246) and FN (785).
