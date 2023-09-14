# Breast-Cancer-CLassification
## Task
Build a Machine Learning model to classify whether the breast cancer is malignant or benign.</br>
Tool Used: Jupyter Notebook, Python

## Dataset
Dataset is taken from Kaggle's "Breast Cancer Wisconsin (Diagnostic) Data Set". The dataset consists of 569 records and 33 features. The feature are:
- ID number
- Diagnosis (M = malignant, B = benign)
- 3-32 features:</br>
  Ten real-valued features are computed for each cell nucleus:
  1. radius (mean of distances from center to points on the perimeter)
  2. texture (standard deviation of gray-scale values)
  3. perimeter
  4. area
  5. smoothness (local variation in radius lengths)
  6. compactness (perimeter^2 / area - 1.0)
  7. concavity (severity of concave portions of the contour)
  8. concave points (number of concave portions of the contour)
  9. symmetry
  10. fractal dimension ("coastline approximation" - 1)</br>
- The mean, standard error and "worst" or largest (mean of the three largest values) of these features were computed for each image, resulting in 30 features. For instance, field 3 is Mean Radius, field 13 is Radius SE, field 23 is Worst Radius.</br>
All feature values are recoded with four significant digits.</br></br>

Source: https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data

## Steps Involved:
### Import the Dependencies
The libraries needed for the task are:
- NumPy
- Pandas
- Logistic Regression from sklearn
- Accuracy Score from sklearn
- Metrics from sklearn
- train test split from sklearn
- Matplotlib
### Data Collection and Analysis
- Load the data from CSV file to Pandas Dataframe using read_csv function
- Use functions as head, shpae, groupby, info and describe function to know more about the dataset
- Check for the missing value.
### Data Processing
- Replace the categorical coulumn to numeric(Benign(B): 0, Malignant(M): 1)
- Split the dataset into features and target where features contains only 'diagnosis' column and features contains rest of the column except id(no use in model training), diagnosis(Target Column) and Unnammed: 32(Contains only NaN).
### Model Building
- Split the dataset into training and test data
- Load the model and train it using training data
- Model Evaluation: Is done on both training and test data and plotted a Confusion matrix for each
  1. Accuracy score for training data:  0.9494505494505494
  2. Accuracy score for test data:  0.9210526315789473
### Build a Predictive System
- Load a random data point from the dataset
- Convert it to Numpy array and reshape it
- Used the built model to predict the outcome and Print the result</br></br></br>
Reference: Project 19. Breast Cancer Classification using Machine Learning | Machine Learning Projects, Siddhardhan, https://www.youtube.com/watch?v=bFh1umUDaGc&list=PLfFghEzKVmjvuSA67LszN1dZ-Dd_pkus6&index=23
