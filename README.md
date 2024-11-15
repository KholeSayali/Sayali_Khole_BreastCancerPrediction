# Sayali_Khole_BreastCancerPrediction
Breast Cancer Prediction Using Machine Learning Techniques.

This code inclueds  machine learning techniques to built application using the Tkinter GUI library in Python. It predicts whether a patient has breast cancer based on certain input features using two machine learning algorithms: Logistic Regression and Random Forest Classifier.

# 1. Dataset
The dataset used is the Breast Cancer dataset from the "sklearn.datasets" module. This is a well-known dataset with labeled features that help predict whether a tumor is malignant or benign.
The dataset contains 30 features, but only the first 5 features are used for simplicity:
  1. mean radius
  2. mean texture
  3. mean perimeter
  4. mean area
  5. mean smoothness
  
# 2. Libraries Required
  1. Tkinter: For creating the GUI application.
  2. Scikit-learn (sklearn): For loading the dataset, building the machine learning models, and data preprocessing.
  3. Numpy: For handling numerical data.
  4. Pandas: For data manipulation and analysis.
  5. Seaborn: For visualizing the target distribution (optional).

# 3. Data Handling
The dataset is loaded using "datasets.load_breast_cancer()".
It is converted into a pandas DataFrame for easier manipulation and analysis.
The first and last 5 rows are displayed using ".head()" and ".tail()".
A count plot is generated using Seaborn to visualize the distribution of the target variable (0: malignant, 1: benign).

# 4. Data Preprocessing
The features (X) are extracted (first 5 features only), and the target labels (y) are assigned.
The dataset is split into training (70%) and testing (30%) sets using train_test_split().
Standardization is applied using StandardScaler() to ensure that the features have a mean of 0 and a standard deviation of 1.

# 5. Model Training
Logistic Regression and Random Forest Classifier are used for training.
The models are trained using the fit() method on the training data (X_train, y_train).

# 6. Evaluation Metrics
  1. Accuracy Score: The percentage of correctly classified samples.
  2. R2 Score: A statistical measure representing the proportion of the variance for the dependent variable that's explained by the     
     independent variables.
  3. Mean Squared Error (MSE): Measures the average of the squares of the errors (differences between predicted and actual values).

# 7. GUI Application (Tkinter)
A simple GUI is created using the Tkinter library.
The user inputs the values for the 5 selected features (mean radius, mean texture, mean perimeter, mean area, mean smoothness).
When the user clicks the PREDICT button, the input data is standardized, and the "Random Forest model" is used to make the prediction.
The prediction result is displayed as:
  "PATIENT HAS NO CANCER (BENIGN)" if the prediction is 0.
  "PATIENT HAS CANCER (MALIGNANT)" if the prediction is 1.
# 8. Output
  1. Console Output: The accuracy, R2 score, and Mean Squared Error for both models (Logistic Regression and Random Forest Classifier) 
     are displayed in the console.
  2. GUI Output: Based on user input, the application predicts whether the patient has cancer or not and displays the result in the GUI 
     window.

# Code Summary
  1. The provided code:
  2. Loads the breast cancer dataset.
  3. Preprocesses the data (feature extraction and standardization).
  4. Trains two machine learning models.
  5. Evaluates the models using common metrics.
  6. Creates a user-friendly GUI for cancer prediction based on input features.
