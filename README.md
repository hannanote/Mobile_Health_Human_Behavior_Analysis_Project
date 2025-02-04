## Mobile_Health_Human_Behavior_Analysis

### Project Overview

The goal of this project is to analyze body motion and vital signs collected from wearable sensors on a group of ten volunteers to classify various physical activities. The MHEALTH dataset is used, which includes sensor data (acceleration, gyroscope, magnetometer, and ECG signals) for different body parts (chest, left ankle, right lower arm) while performing 12 distinct physical activities.

We will use machine learning algorithms to classify these activities and understand how various physiological and motion data correlate with human behavior. This project will demonstrate how wearable technology can be used to monitor and predict physical activity patterns, which can be crucial for health tracking, fitness, and medical applications.
<br>

### Dataset Description:

The MHEALTH dataset consists of 12 signals representing acceleration, gyroscope, and magnetometer data from sensors placed on different parts of the body (chest, left ankle, right lower arm). These signals are captured in three axes: X, Y, and Z.

#### Columns in the Dataset:

Column 0: acceleration from the left-ankle sensor (X axis)

Column 1: acceleration from the left-ankle sensor (Y axis)

Column 2: acceleration from the left-ankle sensor (Z axis)

Column 3: gyro from the left-ankle sensor (X axis)

Column 4: gyro from the left-ankle sensor (Y axis)

Column 5: gyro from the left-ankle sensor (Z axis)

Column 6: acceleration from the right-lower-arm sensor (X axis)

Column 7: acceleration from the right-lower-arm sensor (Y axis)

Column 8: acceleration from the right-lower-arm sensor (Z axis)

Column 9: gyro from the right-lower-arm sensor (X axis)

Column 10: gyro from the right-lower-arm sensor (Y axis)

Column 11: gyro from the right-lower-arm sensor (Z axis)

Column 12: Label (0 for the null class)


#### Physical Activities:

+ Standing still
+ Sitting and relaxing
+ Lying down
+ Walking
+ Climbing stairs
+ Waist bends forward
+ Frontal elevation of arms
+ Knees bending (crouching)
+ Cycling
+ Jogging
+ Running
+ Jump front & back

<br>

### Project Workflow

#### Step 1: Data Preprocessing

Loading Data: Import the dataset using Pandas or similar libraries.

Handling Missing Values: Check for any missing data and decide on imputation or removal.

Normalization: Normalize or standardize the sensor data to ensure the model's convergence.

Feature Selection: Identify which features (e.g., acceleration, gyroscope, magnetometer, ECG) are most relevant for classification.

Splitting Data: Split the dataset into training and testing sets (80% train data, 20% test data).


#### Step 2: Exploratory Data Analysis (EDA)

Visualizing the Data: Plot graphs to visualize the distribution of accelerometer, gyroscope, and ECG signals.

Correlation Analysis: Check for correlations between different sensor readings and the activity labels.

Activity Class Distribution: Analyze the balance of activity labels to identify any class imbalances.

#### Step 3: Model Building

Classification Algorithms: Use various machine learning models such as:
+ Logistic Regression
+ Random Forest
+ Support Vector Machine (SVM)
+ K-Nearest Neighbors (KNN)
+ Neural Networks
+ Hyperparameter Tuning: Use grid search or randomized search for hyperparameter optimization.
+ Cross-validation: Perform cross-validation to evaluate model performance on unseen data.

#### Step 4: Model Evaluation

+ Metrics: Use classification metrics like accuracy, precision, recall, F1-score, and confusion matrix.
+ ROC-AUC: Evaluate the model using the ROC-AUC curve to understand its discriminatory power.

#### Step 5: Model Deployment 

+ Real-Time Prediction: Implement a real-time prediction system for mobile health tracking.
+ User Interface: Build a simple interface to interact with the model (e.g., using Flask or Streamlit).
