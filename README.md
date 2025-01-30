# datascience_health
Supply Chain Machine Learning Analysis

Overview

This project applies Machine Learning (ML) techniques to a dataset from a solder paste inspection process in supply chain management. The dataset includes quality inspection data, machine performance, and board-specific attributes. The goal is to predict soldering quality issues using classification models and analyze key influencing factors.

Dataset Description

The dataset contains 891 observations with the following variables:

Variable

Description

ID

Running number (unique identifier)

QI

Quality Inspection at the end (1 = nIO (not okay), 0 = iO (okay))

Machine

Machine ID performing soldering

PreCheck

Initial quality check before soldering (1 = nIO, 0 = iO)

NumberPins

Number of pins per board

BoardID

Board identifier

Price

Final price in Euros

BoardCategory

Board classification (not further specified)

MaterialOrigin

Origin of solder paste (S = Singapore, C = China, Q = Qatar)

Machine Learning Models Used

The following classification models were applied to predict QI (Quality Inspection result):

Logistic Regression

Decision Tree Classifier

Random Forest Classifier

Additionally, K-Means Clustering was used to group boards based on price and number of pins.

Preprocessing Steps

Converted categorical variables into appropriate formats.

Handled missing values using mean/mode imputation.

Identified and treated outliers using Interquartile Range (IQR).

Scaled numerical features where necessary.

Model Evaluation

Each ML model was evaluated using the following metrics:

Accuracy: Measures overall correctness.

Precision: Proportion of predicted positives that are actually positive.

Recall (Sensitivity): Proportion of actual positives that are correctly predicted.

F1 Score: Harmonic mean of Precision and Recall.

Error Rate: Proportion of incorrect predictions.

Comparison of Classification Methods

Model

Accuracy

Precision

Recall

F1 Score

Error Rate

Logistic Regression

0.80

0.81

0.67

0.73

0.20

Decision Tree

0.75

0.72

0.63

0.67

0.25

Random Forest

0.76

0.75

0.63

0.69

0.24

Visualizations

Confusion Matrices: Heatmaps for each model's classification results.

Feature Importance (Random Forest): Visualizing key variables influencing predictions.

Decision Tree Structure: Graphical representation of the decision-making process.

Box Plots & Histograms: Outlier detection and feature distribution.

Installation & Usage

Requirements

Ensure the following Python packages are installed:

pip install pandas numpy matplotlib seaborn scikit-learn

Run the Code

Clone the repository and execute the script:

git clone https://github.com/yourusername/supply-chain-ml.git
cd supply-chain-ml
python main.py

Conclusion

Logistic Regression performed best overall with 80% accuracy.

PreCheck and MaterialOrigin were among the most significant features.

Random Forest provided better interpretability with feature importance.

This project showcases the power of ML in supply chain quality control, improving defect detection and process optimization.

License

MIT License.

Contact

For questions, contact Your Name at your.email@example.com.

