# # Iris Dataset Classification with KNeighborsClassifier

This project focuses on classifying the different species of Iris flowers based on their physical measurements using the **KNeighborsClassifier** algorithm.

## Project Steps

### 1. Data Loading
- The Iris dataset was downloaded from Kaggle and loaded into a pandas DataFrame.  
- Inspected the first few rows and data types to understand the dataset structure.

### 2. Data Preparation
- Separated features (`X`) and the target variable (`y`).  
- Dropped the `Id` column as it was irrelevant for classification.  
- Split the dataset into training (80%) and testing (20%) sets using `train_test_split`.

### 3. Feature Normalization
- Applied `StandardScaler` to standardize features by removing the mean and scaling to unit variance.  
- This step ensures equal contribution of features since **KNN is sensitive to feature scale**.

### 4. Model Training and Evaluation
- Trained a **KNeighborsClassifier** on normalized training data.  
- Evaluated the model for different values of **K**: 1, 3, 5, 7, and 9.  
- For each K:
  - Calculated accuracy score.
  - Computed the confusion matrix.

### 5. Visualization
- Reduced the test data to two dimensions using **PCA** for visualization.  
- Plotted decision boundaries for the best performing K value (**K=9** in this case).  
- Added a legend to differentiate Iris species.

## Results

- **Accuracy Scores:** The model achieved **1.0000** accuracy for all tested K values.  
- **Confusion Matrices:** Perfect classification — all instances correctly predicted for each K value.

## How to Reproduce

1. Download the Iris dataset from Kaggle.  
2. Install the required dependencies.  
3. Run the Jupyter Notebook or Python script in sequence:
   - Load and prepare the data.
   - Normalize features.
   - Train and evaluate the model for various K values.
   - Visualize decision boundaries.

## Dependencies

- pandas  
- numpy  
- scikit-learn  
- matplotlib  
- seaborn
