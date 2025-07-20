Purpose of Lab Work
This lab investigates and compares the effectiveness of K-Nearest Neighbors (KNN) and Radius Neighbors Classifier (RNN) using the Wine Dataset from sklearn. By analyzing how parameter selection affects classification accuracy, this exercise builds practical skills in data preprocessing, parameter tuning, algorithm evaluation, and result visualization.

🔍 Steps Taken & Code Implementation Explanation
Library Setup & Environment Preparation:

Ensured necessary libraries (scikit-learn, pandas, matplotlib, jupyter) were installed programmatically.

Version checks ensured reproducibility.

Deprecated libraries were noted, and environment setup was automated.

Dataset Loading & Exploration:

Loaded the Wine Dataset using sklearn.datasets.load_wine().

Inspected feature names and target classes.

Analyzed class distribution to ensure balanced learning.

Applied StandardScaler to normalize features, as both KNN and RNN rely on distance-based calculations.

Train-Test Split:

Split dataset into 80% training and 20% testing using train_test_split().

This ensured unbiased evaluation on unseen data.

KNN Classifier Implementation:

Used KNeighborsClassifier from sklearn.

Parameter Choice:

Tested k values: [1, 5, 11, 15, 21].

Selected to explore behavior from minimal neighbors to moderately large neighborhood counts.

Recorded and analyzed accuracy for each k value.

RNN Classifier Implementation:

Used RadiusNeighborsClassifier from sklearn.

Parameter Choice:

Radius values tested: [1.0, 1.5, 2.0, 2.5, 3.0, 3.5].

Focused on small radii due to scaled feature ranges.

Applied outlier_label='most_frequent' to handle radius cases where no neighbors were found.

Visualization:

Created side-by-side line plots:

KNN Accuracy vs. k Value

RNN Accuracy vs. Radius Value

Graphs were clearly labeled with axis titles and gridlines for easy interpretation.

Performance Comparison:

Printed accuracy tables.

Identified best-performing parameters for both models.

Discussed model preference based on trends and parameter sensitivity.

⚙️ Parameter Choices Reasoning
KNN (k values):

Covered small to moderately large neighbor counts to study accuracy stability and detect potential overfitting or underfitting.

RNN (radius values):

Chosen considering scaled feature distances.

Smaller radii ensured meaningful neighbor selection.

Outlier labeling prevented errors during predictions at smaller radii.

📊 Results Interpretation
KNN Results:
Stable accuracy (~0.944).

Best accuracy: 0.9722 at k = 15.

Performance consistent across tested k values.

RNN Results:
Performance improved sharply with increasing radius.

Best accuracy: 1.0000 at radius = 3.5 (perfect classification).

RNN showed sensitivity to radius selection.

📈 Visualizations
Line plots clearly communicate how parameter variations affect accuracy for each model.

Plots are:

Clean and well-labeled.

Easy to interpret.

Useful in highlighting trends, outliers, and optimal parameters.

📌 Comparison Summary & Insights
| Model | Best Parameter | Best Accuracy | Observations                                            |
| ----- | -------------- | ------------- | ------------------------------------------------------- |
| KNN   | k = 15         | 0.9722        | Stable, reliable performance. Less sensitive to tuning. |
| RNN   | radius = 3.5   | 1.0000        | Superior performance but sensitive to radius selection. |


Recommendations:

Choose KNN for general-purpose classification tasks requiring stable, predictable performance with minimal tuning.

Choose RNN when maximizing accuracy is essential, and tuning efforts can be dedicated to radius optimization.

📁 Repository Structure
MSCS_634_Lab_2.ipynb: Complete notebook containing:

Full code implementation.

Clear code comments and explanations.

Data exploration and preprocessing.

Model training and evaluation.

Visualizations and performance analysis.

README.md: This document summarizing objectives, methodology, analysis, and findings.

🏁 Conclusion
Through this lab, the following skills and knowledge were developed:

Distance-based model implementation (KNN, RNN).

Feature scaling for algorithm optimization.

Parameter tuning with clear reasoning.

Visualization and interpretation of machine learning results.

Comparative analysis leading to informed model choice.

Ultimately, RNN achieved the highest accuracy but required careful tuning, while KNN demonstrated stable and reliable performance.

