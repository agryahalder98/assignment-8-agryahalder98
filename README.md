
# DA5401: Ensemble Learning for Complex Regression Modeling on Bike Share Data
### Name: AGRYA HALDER

### Roll: ED25D900

This structure covers the project's purpose, the data used, the methods applied, and the key findings.




This project explores the application of various **ensemble learning techniques** (Bagging, Boosting, and Stacking) to predict **hourly bike rental counts** using the Bike Sharing Dataset (sourced from UCI Machine Learning Repository).

The goal is to demonstrate how advanced ensemble methods can overcome the limitations of single models (like Decision Trees) by effectively managing the **Bias-Variance Tradeoff** to achieve superior generalization and predictive accuracy in a real-world regression task.



## Project Structure

* `DA5401 A8_ED25D900.ipynb`: The main Jupyter Notebook containing all data loading, preprocessing, model training, evaluation, and comparative analysis.
* `README.md`: This file.



## Methods and Models Implemented

The analysis follows a comprehensive modeling pipeline, comparing single models against increasingly sophisticated ensembles:

### 1. Baseline Model
* **Decision Tree Regressor:** Used as a high-variance, low-bias baseline to demonstrate the problem of overfitting.

### 2. Variance Reduction (Bagging)
* **Bagging Regressor:** Utilizes multiple Decision Trees trained on bootstrap samples to reduce variance.
* *Expected Outcome:* Significant reduction in **RMSE** compared to the single Decision Tree.

### 3. Bias Reduction (Boosting)
* **Gradient Boosting Regressor:** Sequentially trains shallow trees to correct the residuals (errors) of previous models, primarily focusing on reducing **bias**.
* *Expected Outcome:* Major improvement in **RMSE** and **R²** over the baseline.

### 4. Advanced Ensemble (Stacking)
* **Stacking Regressor:** Combines predictions from diverse base learners (e.g., K-Nearest Neighbors, Decision Tree, Linear Model) using a **meta-learner (Ridge Regression)** to find the optimal weighted combination.
* *Expected Outcome:* Superior performance, reducing both bias and variance more effectively than single ensemble methods.


## Key Findings

The results confirm the efficacy of ensemble learning in complex regression:

| Model Type | Primary Target | Sample RMSE | Sample R² | Performance Implication |
| :--- | :--- | :--- | :--- | :--- |
| **Single Decision Tree** | Baseline | ~118.46 | - | High Variance (Overfitting) |
| **Bagging Regressor** | Variance | ~112.36 | ~0.60 | Improved stability and generalization. |
| **Gradient Boosting** | Bias | **~67.06** | **~0.85** | Major error reduction; high predictive power. |
| **Stacking Regressor** | Bias & Variance | **~66.80** | **~0.86** | Achieves the best overall generalization. |

* **Boosting** achieved the most significant leap in performance, validating its role in capturing complex, non-linear patterns (Bias Reduction).
* **Stacking** yielded the absolute best result by intelligently combining the complementary strengths of diverse algorithms, highlighting its potential for maximizing prediction accuracy.



## Installation and Execution

To run this notebook, you will need a Python environment with the following libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn ucimlrepo
````

1.  Clone the repository:
    ```bash
    git clone [Your Repository URL]
    ```
2.  Navigate to the project directory.
3.  Open and run the `DA5401 A8_ED25D900.ipynb` notebook in Jupyter or a compatible environment.


