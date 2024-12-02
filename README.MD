# Experimental Projects - A.Y. 2023/2024

This repository contains the implementation of **Project 2: Tree Predictors for Binary Classification**, as part of the experimental projects for the academic year 2023/2024. The goal of this project is to implement tree predictors from scratch for binary classification using the Mushroom dataset. The task is to determine whether mushrooms are poisonous based on the features in the dataset.

## Submission Details

- **Deadline for submission**: 17/02/2025
- **Oral Examination**: Approximately within 2-3 weeks after the submission deadline.
- **Individual work**: Group projects are not allowed. All students must complete the project individually.

## Project Guidelines

This project requires you to follow the methodology outlined below:

### 1. Data Preprocessing
- Carefully preprocess the data and ensure that no information from the test set is used during the training phase.
- Avoid manipulating data that would bias the performance evaluation.

### 2. Model Implementation
- Implement tree predictors from scratch for binary classification.
- The tree predictors must use single-feature binary tests as decision criteria at internal nodes.
    - For numerical/ordinal features: use thresholds.
    - For categorical features: use membership tests.

#### Node Class Implementation
Implement a class/structure for the nodes of the tree:
- **Attributes**:
  - Constructor to initialize the node (empty or with given attributes).
  - Left and right children (both should be nodes themselves).
  - A flag indicating whether the node is a leaf.
  - Decision criterion/test (a function that takes a data point as input and returns a Boolean output).

#### Tree Class Implementation
Implement a class/structure for the binary tree predictor:
- **Attributes**:
  - Constructor initializing the tree with decision criteria for each feature.
  - Splitting criterion for selecting both the leaf to expand and the decision criterion (e.g., Gini index, scaled entropy).
  - Stopping criterion to halt the tree construction (e.g., maximum depth, maximum nodes, weight constraints on leaves).
- Procedure for training the tree predictor on the training set.
- Procedure to evaluate the predictor on a test set.

### 3. Hyperparameter Tuning
- Tune the tree predictor's hyperparameters, such as splitting and stopping criteria.
- The tuning must be done carefully, ensuring a sound methodology.
- Conduct hyperparameter tuning for at least one of the tree predictors.

### 4. Evaluation and Results
- Train at least 3 tree predictors with different splitting criteria.
- Implement at least 2 stopping criteria and evaluate the performance of each tree.
- Compute the training error for each tree based on the 0-1 loss.
- Write a report discussing the performance of each model, including:
  - Methodology and rationale behind chosen hyperparameters.
  - Discussion of overfitting or underfitting.
  - Computational costs.

#### Optional: Random Forest
- Implement a random forest classifier by reusing the previously implemented tree predictor class/structure.

## Report Guidelines

Your report must include the following sections:

- **Introduction**: Overview of the project and goals.
- **Methodology**: Detailed discussion of the tree predictor implementation, including decisions made during the data preprocessing and model training phases.
- **Results**: Comprehensive evaluation of each model, including performance metrics and any observed overfitting or underfitting.
- **Conclusion**: Insights into the project, including how overfitting was handled (e.g., through pruning or stopping criteria) and the computational costs.

## Resources

For further reading, the following resources are suggested:

- Chapter 18 of the book “_Understanding Machine Learning: From Theory to Algorithms_” by Shalev-Shwartz and Ben-David.
- Section 9.3.3 of the book “_Foundations of Machine Learning_” by Mohri, Rostamizadeh, and Talwalkar.
- The Decision Forests course by Google for Developers.

## License

This project is intended for educational purposes only. All code is to be written by the student and submitted individually as per the course guidelines.
