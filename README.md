# Bank-Personal-Loan-Conversion-Prediction

## Conclusion and Model Results Interpretation

In the previous year, Thera Bank conducted a campaign targeting liability customers, achieving a remarkable conversion rate of over 9% success.

Most machine learning models excel when classes are evenly distributed, as they are designed to optimize accuracy and minimize errors. However, these models often overlook class distribution or class balance. In our dataset, only 9.6% of customers accepted the bank's loan offer (class 1), while 90.4% declined (class 0).

### Understanding the Metrics

The confusion matrix is a vital metric for evaluating classification algorithms, providing insights into actual and predicted classes. Key metrics derived from the confusion matrix include:

- **Precision**: Measures the accuracy of positive predictions and minimizes false positives.
- **Recall**: Gauges how effectively the model predicts actual positives and minimizes false negatives.
- **F1-score**: A harmonic mean of precision and recall.

### Evaluation Metrics and Model Performance

| Models      | Recall Score for Class 1 (%) | F1-score for Class 1 (%) | ROC AUC (%) | Accuracy (%) |
|-------------|--------------------------|----------------------|-----|----|
| **Logistic Regression** | 53 | 64 | 76 | 94.2 |
| **Logistic Regression with Hyperparameter Tuning** | 55 | 64 | 77 | 94 |
| **k-Nearest Neighbor without Feature Scaling** | 30 | 39 | 64 | 90.7 |
| **k-Nearest Neighbor with Feature Scaling** | 63 | 76 | 81 | 96.1 |
| ***k-Nearest Neighbor with Feature Scaling and Hyperparameter Tuning*** | ***66*** | ***79***| ***83*** | ***96.5*** |
| **Naive Bayes** | 59 | 52 | 76 | 89.3 |

### Model Selection and Advantages of k-Nearest Neighbor (k-NN)

It's evident that the **k-Nearest Neighbor with Feature Scaling and Hyperparameter Tuning** model excels, boasting superior recall (66%), F1-score (79%), ROC AUC (83%), and Accuracy (96.5%) compared to other models. Several factors contribute to its success:

- Being non-parametric, k-NN doesn't require strict data assumptions, unlike parametric models like logistic regression.
- Its memory-based approach allows adaptability to changing input data in real-time.
- k-NN excels with a small number of input variables, an advantage we leveraged after eliminating irrelevant features.

### Addressing Class Imbalance with Oversampling (SMOTE)

Additionally, we explored **oversampling** as a strategy to address class imbalance. Among the various techniques, we adopted the Synthetic Minority Over-Sampling Technique (SMOTE). SMOTE's unique advantage lies in generating synthetic observations, reducing the risk of overfitting compared to traditional random over-sampling.

The results of applying SMOTE in conjunction with the best-performing model, k-NN with feature scaling and hyperparameter tuning, are remarkable:

* **Recall (class 1): 75% (a notable improvement of 9%)**
* **F1-score (class 1): 83% (a significant improvement of 4%)**
* **ROC AUC score: 87% (a substantial improvement of 4%)**
* **Accuracy Score: 97% (an impressive improvement of 0.5%)**

### Robustness and Concluding Remarks

It's important to highlight that both the k-NN model with feature scaling and hyperparameter tuning and the oversampled variant showed no signs of overfitting or underfitting, emphasizing the robustness of these approaches.

---

Feel free to customize this README content as needed and then upload it to your GitHub repository.
