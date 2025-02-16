## Mobile_Health_Human_Behavior_Analysis

### Project Overview

Mobile health (mHealth) is an emerging field in digital health that utilizes mobile technology to provide care and treatment to individuals. With the increasing prevalence of smart devices, human behavior, particularly in relation to health, has become more quantifiable. This presents both an opportunity and a challenge in predicting human behavior from daily activities.

Human behavior is complex and multifaceted, and predicting it is difficult. However, with the use of sensor data from devices like accelerometers, gyroscopes, and other health monitoring technologies, it becomes possible to analyze and predict human behavior. By capturing body motion and vital signs, we can derive valuable insights that support personalized health management.
<br>

### Dataset Description

The dataset used in this project is the **MHEALTH (Mobile Health) dataset**, which includes data from ten volunteers performing 12 distinct physical activities. The data includes accelerometer and gyroscope readings captured by sensors placed on the volunteers' chest, right wrist, and left ankle, which measure acceleration, angular velocity, and magnetic field orientation.

This dataset is provided by the UCI Machine Learning Repository:

[**MHEALTH Dataset**](https://archive.ics.uci.edu/dataset/319/mhealth+dataset)


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
