# Task-4
📂 Dataset
File: Housing.csv

Contains various house-related features such as number of bedrooms, area, presence of facilities, and furnishing status.

Target variable: price (converted to binary — above or below median)

⚙️ Steps & Workflow
1. Import Libraries
Uses essential libraries:

pandas, numpy

matplotlib, seaborn

sklearn for ML processing, modeling, and evaluation

2. Data Preprocessing
Binary encoding of columns: yes/no → 1/0

One-hot encoding of furnishingstatus

Drop missing values

Create binary target:

python
Copy code
target = 1 if price > median_price else 0
Drop original price column

3. Model Training
Features scaled with StandardScaler

Split into training and testing sets (80/20)

Trained a LogisticRegression model

4. Evaluation Metrics
Classification Report:

markdown
Copy code
             precision    recall  f1-score   support
         0       0.80      0.92      0.85        51
         1       0.92      0.79      0.85        58
     Accuracy = 0.85
Confusion Matrix
Visualized using Seaborn heatmap

ROC-AUC Curve
AUC = ~0.91

5. Threshold Tuning
Custom threshold of 0.4 used

Updated confusion matrix:

lua
Copy code
[[44  7]
 [10 48]]
🧠 Concepts Covered
Logistic Regression: Classification algorithm that uses the sigmoid function to output probabilities.

Feature Scaling: Required for better model convergence and accuracy.

Evaluation Metrics:

Precision, Recall, F1-score

Confusion Matrix

ROC-AUC

📊 Visualization
Confusion Matrix (seaborn.heatmap)

ROC Curve with threshold-tuned classification
