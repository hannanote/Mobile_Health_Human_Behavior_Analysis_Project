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

**Project Approach**

The key steps in the project were:

1. **Data Retrieval**: Downloading the dataset and organizing it for analysis.
2. **Data Preparation**: Preprocessing the data.
3. **Data Visualization**: Performing Exploratory Data Analysis (EDA) to visualize patterns and trends.
4. **Model Training**: Training multiple machine learning models to predict human behavior based on the dataset.
5. **Model Evaluation**: Evaluating the performance of each model based on various metrics.
6. **Model Deployment**: Deploying the best model for live predictions.

**Machine Learning Models Used**

The models used in this project include:

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Support Vector Classifier (SVC)
- Random Forest Classifier
- Decision Tree Classifier
- Neural Network

### **Model Evaluation**

When evaluating the models on the training data, various performance metrics were used, including **Recall**, **Specificity**, **Precision**, **Balanced Accuracy**, and **F1-Score**. The table below summarizes the performance of each model on the training dataset:

| Model | Recall | Specificity | Precision | Balanced Accuracy | F1-Score |
| --- | --- | --- | --- | --- | --- |
| Logistic Regression | 0.581 | 0.999 | 0.609 | 0.614 | 0.571 |
| K-Nearest Neighbors (KNN) | 0.979 | 1.000 | 0.987 | 0.986 | 0.982 |
| Support Vector Classifier | 0.758 | 0.999 | 0.759 | 0.758 | 0.744 |
| Random Forest Classifier | 0.902 | 0.999 | 0.905 | 0.902 | 0.901 |
| Decision Tree Classifier | 0.848 | 1.000 | 0.851 | 0.848 | 0.846 |
| Neural Network | 0.898 | 1.000 | 0.901 | 0.916 | 0.897 |

From the table, **K-Nearest Neighbors (KNN)** emerged as the top-performing model with the highest F1-Score of 0.982, followed closely by **Random Forest** and **Neural Network**, both of which showed strong performance as well.

### **Test Data Results**

For the test dataset, the **K-Nearest Neighbors (KNN)** model was chosen, and the following results were obtained:

- **Accuracy**: 98.4%
- **Specificity**: 100%
- **Recall**: 97.6%
- **Precision**: 98.5%
- **F1-Score**: 98.0%

These results demonstrate that the KNN model performed exceptionally well, maintaining high accuracy and a balanced approach to precision and recall.

<img src='https://github.com/user-attachments/assets/144281bc-e049-421a-929a-c0ac1d97e3d7' width='700px' height='400px'>



### **Cross-Validation Results**

In order to validate the performance of the KNN model further, **cross-validation** was performed using the **cross_val_score** function. The accuracy obtained from cross-validation was 97.2%, confirming that the model generalizes well to unseen data.

### **AUC Scores and Class Imbalance**

In addition to the performance metrics, the **Area Under the Curve (AUC)** values were also computed for each class to evaluate the model's ability to discriminate between different activity classes. The AUC values for each class are as follows:

![Image](https://github.com/user-attachments/assets/6cfc1e00-6444-44f0-85e5-d58af6b7e106)

|  | AUC | 0.999 |
| --- | --- | --- |
| Class 2 | AUC | 1.000 |
| Class 3 | AUC |  1.000 |
| Class 4 | AUC | 0.991 |
| Class 5 | AUC | 0.984 |
| Class 6 | AUC | 0.990 |
| Class 7 | AUC | 0.997 |
| Class 8 | AUC | 0.981 |
| Class 9 | AUC | 1.000 |
| Class 10 | AUC | 0.995 |
| Class 11 | AUC | 0.997 |
| Class 12 | AUC | 0.993 |

### **Conclusion**

The K-Nearest Neighbors (KNN) model performed exceptionally well in predicting human activity and behavior, achieving high accuracy (98.4%) and strong metrics across recall, precision, specificity, and F1-Score. The model also performed well in cross-validation with an accuracy of 97.2%. However, the high AUC values, particularly the perfect scores for some classes, may indicate class imbalance within the dataset, which could inflate the performance metrics.

Despite this, the project successfully demonstrated the potential of machine learning models, especially KNN, for predicting human behavior using mobile health data. This has important implications for the development of mobile health applications that can monitor and predict user activities, potentially enhancing personalized health interventions.
