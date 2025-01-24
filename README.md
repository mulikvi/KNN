# Custom RandomSearchCV Implementation
This project implements a custom version of RandomSearchCV for hyperparameter tuning, using the K-Nearest Neighbors (KNN) classifier. It demonstrates hyperparameter selection by evaluating model performance across multiple folds of cross-validation and visualizes decision boundaries to understand the classifier's behavior.

<b>Features</b><br>
Implements a custom RandomSearchCV function to:<br>
  1)Generate random hyperparameters for KNN (number of neighbors).<br>
  2)Perform cross-validation on training data.<br>
  3)Calculate train and test accuracies for each hyperparameter.<br>
  4)Identify the optimal hyperparameter value.<br>
  5)Visualizes the relationship between hyperparameters and model accuracy.<br>
  6)Plots decision boundaries for the best hyperparameter to showcase classification results.



<b>Dataset</b><br>
The dataset is synthetically generated using sklearn.datasets.make_classification. It contains:<br>
	                  10,000 samples<br>
	                  2 informative features<br>
	                  Binary classification with balanced classes


<b>Dataset Preparation:</b><br>
The dataset is split into training and testing sets using train_test_split with stratified sampling to maintain class balance.

<b>Custom RandomSearchCV:</b><br>
  The function evaluates 10 randomly selected hyperparameter values in the given range.Performs k-fold cross-validation for each hyperparameter.Returns the train and test accuracies for each hyperparameter.

<b>Visualization:</b><br>
  Plot the hyperparameter vs. accuracy curve to identify the best parameter.
  Visualize decision boundaries using the plot_decision_boundary function.

Hyperparameter vs. Accuracy Plot: Displays train and test accuracy for each hyperparameter value.
Best Hyperparameter: The best k value (e.g., k = 23) is determined from the plot.
Decision Boundary: Visualizes the classification regions for the best k value.

<b>Key Functions</b><br>

<b>RandomSearchCV:</b><br>
Inputs: Training data, classifier, parameter range, and folds.<br>
Outputs: Train and test accuracies, hyperparameter values.


<b>plot_decision_boundary:</b><br>
Inputs: Features, labels, and classifier.<br>
Output: Visualizes decision boundaries for the given classifier.


<b>Dependencies</b><br>
numpy<br>
scikit-learn<br>
matplotlib<br>
tqdm

