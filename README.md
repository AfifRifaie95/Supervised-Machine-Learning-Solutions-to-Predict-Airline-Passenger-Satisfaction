# Supervised-Machine-Learning-Solutions-to-Predict-Airline-Passenger-Satisfaction
## Abstract
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
<img width="811" alt="image" src="https://github.com/user-attachments/assets/6c22d094-e56f-474d-8648-15bd882f6877" />

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

<img width="807" alt="image" src="https://github.com/user-attachments/assets/3bfafcbb-d152-4378-8761-422616b548a9" />
                                      
                                      Table 2: Confusion Matrix Evaluation

The tuned Gradient Boosting confusion matrix also shows better precision and recall, it shows
enhanced performance and better generalization across all models. It achieved TN (11,451)
and TP (8,299) while reducing FP (246) and FN (785).

# Analysis
Based on the model’s output, Gradient Boosting was expected to perform best in this report
and followed by Random Forest and KNN. The result is aligned with our expectation. As stated
earlier, Gradient Boosting refines predictions by sequentially minimizing errors (residuals)
from prior iteration, result as a strong predictive model. It also has ability to process intricate
data structure and integrate diverse feature dimension effectively. This makes it effective at
handling high-dimension data and capturing complex feature interactions in airline
satisfaction survey dataset.

In addition to that, both Random Forest and Gradient Boosting have flexibility, however,
Gradient Boosting offer more flexibility and options for hyperparameter tuning. the primary
hyperparameter (RandomizedSeachCV and GridSearchCV) is tuned for Gradient boosting in
this report is n_estimator, which to control the total number of sequential models to fit.
learning_rate, which to how much to learn each boosting stage, max_features, set the number
of features to consider at each stage. subsample, established the percentage of data to train
on at each stage. max_depth and min_sample_leaf.

With greater number of flexibilities, comes with greater computational cost and time
consuming when dealing with large dataset and complex models. GridSearchCV performs an
exhaustive search over a specified parameter grid. It evaluates all possible combinations of
hyperparameter values. It is however, the computational cost grows exponentially with the
number of hyperparameters and their possible values (Keylabs, 2024). RandomizedSearchCV,
on the other hand, offers a more efficient alternative by randomly sampling a fixed number of
combinations from the hyperparameter space. This approach reduces the computational
burden as it allows users to control the number of iterations. Despite its advantages,
RandomizedSearchCV may not always find the absolute best hyperparameter combination
due to its randomness. it often provides a near-optimal solution much faster, which can be
refined further using GridSearchCV over a narrowed range of promising hyperparameters
(Brown, 2024). This report utilised GridSearchCV that provides near optimal solution much
faster and then refined by using GridSearchCV over a narrowed range of promising
hyperparameter. This approach can reduce computational power and time.

Interesting finding in this report is the base KNN is performing well with high score matrix,
which is unexpected, given its simplicity. This could be due to proper data pre-processing such
formatting the data, remove any missing values, outliers, feature one hot encoding can
significantly impact KNN’s performance. In addition to that, critical roles of feature scaling with
standardscaller, which process of normalizing the independent variables, fully optimized
KNN’s performance. It ensures all features avoid bias and improve predictive accuracy. It is
important to note that decision trees based such as Random Forest and Gradient Boosting do
not require feature scaling. which split data based on feature thresholds and are insensitive
to the scale of the input features. Hence the scaling was excluded in Random Forest and
Gradient Boosting for this report.

In addition to that, it also true the tuning may not drastically improve result when pre-
processing is optimized. Theoretically, hyperparameter tuning should improve model
performance by finding the optimal configuration for a given dataset. However, when pre-
processing has already extracted, the room for improvement through hyperparameter tuning
is reduced. This is particularly true for KNN, where the algorithm's performance is closely tied
to the distance calculations, which are directly influenced by the quality of the input data. In
this example, KNN’s output, despite undergoing hyperparameter tuning, achieves 1% training
accuracy, raises significant concerns. It’s a clear indicator of underfitting. An underfitted model
with 1% training accuracy suggests that the hyperparameter tuning process has not been
effective or that the model's complexity is insufficient to capture the data's nuances
(CatarinaG, 2024)
