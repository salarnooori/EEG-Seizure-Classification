# EEG Seizure Detection Using Machine Learning
This project implements three different classification methods on the EEG Scalp MIT-CHB sub-dataset to classify seizure and non-seizure events. The dataset includes recordings from 5 subjects, each with 5 seizure cases and 1 non-seizure case.

Data Preparation
Data Reading: The data and summary texts explaining seizure times are read to make the first trial.

Sample Seizure and Non-Seizure Signals: [Placeholder for sample signals]
Segmentation: Trials are segmented by cropping 10-minute records with frequencies before the start time of seizures for each sample. An equal number of 10-minute segments are selected from non-seizure cases.

Sample Segments: [Placeholder for segmented signals]
Epoch Creation: 16-second epochs are created from the first 9 minutes of each signal sample.

Sample Epochs: [Placeholder for epochs]
Feature Extraction and Selection
Features such as Shannon entropy, variance, minimum, maximum, and mean are extracted.
Features are normalized using Z-score.
Feature selection is performed using T-test, selecting features with a p-value smaller than 0.001 per subject.
Classification Methods
Three classification methods are implemented and evaluated:

Radial Basis Function (RBF) Network:

Best K is determined using K-means clustering and silhouette scores.
Centers found are used as neurons in the hidden layer of the RBF.
Classification is done using a weight matrix during training.
K-Nearest Neighbors (KNN)

Support Vector Machine (SVM)

Evaluation
Accuracy, Sensitivity, Specificity: Calculated for each subject across the three methods.
Parameter Evaluation:
Changing Sigma in RBF: Evaluated in the range of (-0.5, -0.25, 0.25, 0.5).
Training vs Testing Size: Evaluated in the range of (0.4, 0.2, 0.1, 0.05) for test_size.
P-value Threshold for Feature Selection: Evaluated in the range of (0.01, 0.001, 0.0001).
Results
The results are presented in terms of accuracy, sensitivity, and specificity for each classification method and subject, highlighting the effectiveness of each approach in detecting seizures from EEG signals.

Full Report
For a detailed report on the implementation and results, please refer to [Report](Report.pdf) .
