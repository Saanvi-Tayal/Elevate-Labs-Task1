# K-Nearest Neighbors (KNN) Classifier on Iris Dataset

This project demonstrates the application of the K-Nearest Neighbors (KNN) classification algorithm using Python's `scikit-learn` library. It covers data normalization, model training, hyperparameter tuning (K value), performance evaluation, and visualization of decision boundaries and feature importance.

## Project Steps:

1.  **Dataset Selection and Feature Normalization:**
    * The **Iris dataset** was chosen for this classification task. This classic dataset contains measurements of iris flowers and their corresponding species.
    * **Numerical features** (sepal length, sepal width, petal length, petal width) were normalized using `MinMaxScaler`. This scales all features to a range between 0 and 1, which is crucial for distance-based algorithms like KNN to prevent features with larger scales from disproportionately influencing the distance calculations.

2.  **KNeighborsClassifier Implementation:**
    * The `KNeighborsClassifier` from `sklearn.neighbors` was used to build the classification model.
    * The dataset was split into training and testing sets (70% training, 30% testing) to evaluate the model's generalization performance on unseen data.

3.  **Experimentation with Different K Values:**
    * The performance of the KNN model was explored by varying the number of neighbors (`K`) from 1 to 20.
    * For each `K` value, the model was trained, and its accuracy was recorded on both the training and test sets.
    * A plot visualizing "Accuracy vs. K Value" was generated to identify the optimal `K` that yields the best balance between bias and variance (typically maximizing test accuracy).

4.  **Model Evaluation:**
    * The model's performance (using the optimal or a chosen `K`) was evaluated using standard classification metrics:
        * **Accuracy Score:** The proportion of correctly classified instances.
        * **Confusion Matrix:** A table showing the number of correct and incorrect predictions made by the classification model, broken down by each class.

5.  **Visualization of Decision Boundaries:**
    * To understand how the KNN model separates different classes, decision boundaries were visualized.
    * As 4D visualization is not possible, the model's behavior was plotted using two key features: 'petal length (cm)' and 'petal width (cm)', which are highly discriminative in the Iris dataset.
    * The plot displays the decision regions (areas where the model predicts a certain class) along with the actual data points, providing insight into the model's classification logic.

6.  **Feature Importance (Permutation Importance):**
    * While KNN doesn't inherently provide feature importance like tree-based models, **Permutation Importance** was used to estimate the contribution of each feature to the model's predictive power.
    * This method assesses how much the model's accuracy decreases when the values of a single feature are randomly shuffled. A larger decrease indicates higher importance.
    * A box plot of feature importance scores was generated to visually compare the influence of each feature.

---

**Technologies Used:**

* **Python**
* **pandas** (for data manipulation)
* **scikit-learn** (for machine learning models, preprocessing, and evaluation)
* **matplotlib** (for plotting and visualization)
* **seaborn** (for enhanced plot aesthetics)