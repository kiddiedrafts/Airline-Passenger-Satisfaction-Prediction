# Hotel Satisfaction Prediction
This project aims to predict customer satisfaction based on flight-related features. Various machine learning models, including K-Nearest Neighbors (KNN) and Random Forest, are assessed for their effectiveness in predicting passenger satisfaction, alongside a deep learning model using Keras to classify whether a customer is satisfied or not, while also comparing the performance of the models.

## Dataset

This dataset contains customer feedback on airline services. It includes passenger details (such as gender, age, and customer type), flight details (such as distance and class), and ratings for various services (such as seat comfort, check-in service, in-flight Wi-Fi, food and beverages, and delays). The main goal of using this dataset is to predict passenger satisfaction (satisfied or neutral/dissatisfied) based on these features.

## Data Preprocessing

The dataset is preprocessed to handle missing values, encode categorical variables, and standardize numerical features.

### Steps:

#### Handling Missing Values:

Missing values in the `Arrival Delay in Minutes` column are filled with the median value.

#### Encoding Categorical Variables:

Categorical features like `Gender`, `Customer Type`, `Type of Travel`, and `Class` are encoded using Label Encoding.


#### Standardizing Numerical Features:

Numerical features are standardized using `StandardScaler` to improve model performance.


## Exploratory Data Analysis (EDA)

Several visualizations are created to understand the data distribution and relationships between features.

### Key Visualizations:

- Correlation Matrix Heatmap
- Scatter Plot for Delays
- Box Plots for Features


## Models Used:

### 1. k-Nearest Neighbors (KNN)
- A simple baseline model that classifies passengers based on the majority vote of their nearest neighbors.  

### 2. Random Forest
- A more advanced ensemble learning method using multiple decision trees to improve prediction accuracy.  

### 3. Deep Neural Network (DNN)
- A neural network with two hidden layers (each with 128 neurons) and dropout regularization to prevent overfitting.  
- Uses the **ReLU** activation function for hidden layers and **sigmoid** activation for the output layer.  
- Trained for 100 epochs with a batch size of 128. Early stopping is used to prevent overfitting.

By comparing these models, we assess the trade-offs between simplicity, interpretability, and performance, ultimately aiming to find the most effective approach for predicting passenger satisfaction.


## Evaluation

Models were evaluated based on **accuracy** and **ROC AUC** and achieved the following scores:

- **KNN:** **92.77% accuracy** on the validation set.
- **Random Forest:** **96.34% accuracy** on the validation set.
- **Deep Neural Network (DNN):**  
  - training set: **0.979** 
  - test set: **0.957**

