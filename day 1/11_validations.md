### 1. Train-Test Split

**Purpose**: To evaluate model performance on unseen data by splitting the dataset into training and test sets.

- **Method**: 
  - **Splitting**: Randomly divide the dataset into two portions: typically, 70-80% for training and 20-30% for testing.
  - **Training**: Fit the model on the training set.
  - **Testing**: Evaluate the model on the test set using predefined evaluation metrics.
  
- **Advantages**:
  - Simple and easy to implement.
  - Provides a quick estimate of model performance on unseen data.

- **Limitations**:
  - Results can vary depending on the random selection of data points.
  - Limited data for training and evaluation.

### 2. k-fold Cross Validation

**Purpose**: To validate model performance by splitting the dataset into k subsets (folds) and iteratively using each fold as a validation set while the remaining data as training sets.

- **Method**:
  - **Splitting**: Divide the dataset into k folds of equal size.
  - **Iterative Training**: Perform training and evaluation k times, each time using a different fold as the validation set and the remaining k-1 folds as the training set.
  - **Aggregating Results**: Average the evaluation metrics across all k iterations to obtain a final performance estimate.

- **Advantages**:
  - Reduces variability in performance estimation compared to a single train-test split.
  - Maximizes the use of data for training and validation.

- **Limitations**:
  - Computationally more expensive than a simple train-test split, especially for large datasets or complex models.

### 3. Leave-One-Out Cross Validation

**Purpose**: A special case of k-fold cross-validation where k equals the number of instances in the dataset, leaving one instance out as the validation set in each iteration.

- **Method**:
  - **Iterative Process**: For each instance in the dataset, use it as the validation set and the remaining instances as the training set.
  - **Evaluation**: Compute performance metrics for each iteration and aggregate them.

- **Advantages**:
  - Provides a less biased estimate of model performance, especially with smaller datasets.
  - Utilizes all data points for training and validation.

- **Limitations**:
  - Can be computationally expensive, especially for large datasets.
  - Results can be sensitive to outliers or specific data distributions.

### 4. Stratified k-fold Cross Validation

**Purpose**: Similar to k-fold cross-validation but preserves the percentage of samples for each class in each fold, ensuring each fold is representative of the overall dataset.

- **Method**:
  - **Stratification**: Ensure that each fold has approximately the same percentage of samples for each class as the original dataset.
  - **Advantages**: 
      Ensures that the model is trained and evaluated on representative samples from the entire dataset
