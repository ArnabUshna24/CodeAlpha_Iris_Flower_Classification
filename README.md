# Iris Flower Classifier


## Overview
Iris flower has three (3) species - Setosa, Versicolor, and Virginica. They differ according to their measurements, i.e., sepal length, sepal width, petal length, and petal width. The goal of this project is to classify a sample Iris flower from the provided measurements according to the species by training an ML model that can learn from the given dataset and do the classification.

## Data Extraction
This dataset is available on [Kaggle](https://www.kaggle.com/datasets/saurabh00007/iriscsv), which consists of 150 Iris flower measurement data. It has 6 columns - `Id`, `SepalLengthCm`, `SepalWidthCm`, `PetalLengthCm`, `PetalWidthCm`, and	`Species`. After importing all the necessary libraries, Google Drive was mounted to access the dataset. As there were no missing values, data preprocessing was not required.

<table>
  <tr>
    <td align="center"><img src="https://github.com/ArnabUshna24/CodeAlpha_Iris_Flower_Classification/blob/main/data_visualizations/distribution_iris_species.png" alt="Iris Species" width="400"/></td>
    <td align="center"><img src="https://github.com/ArnabUshna24/CodeAlpha_Iris_Flower_Classification/blob/main/data_visualizations/distribution_iris_features.png" alt="Iris Features" width="500"/></td>
  </tr>
  <tr>
    <td align="left"> Fig. 1: Distribution of Iris species </td>
    <td align="left"> Fig. 2: Distribution of Iris features </td>
  </tr>
</table>

## Feature and Target Preparation
After importing `LabelEncoder` from `sklearn.preprocessing` package, `Species` column was encoded into numeric labels. Other columns (except `Id`) were selected as feature columns. After that, data was split into training (80%) and testing (20%) categories. Also, the features were scaled.

## Model Training and Evaluation
For this project, `RandomForestClassifier` was used.

<p><strong>Table 1:</strong> Class-wise Performance Metrics </p>
<table border="1" cellspacing="0" cellpadding="5">
  <tr>
    <th align="left"> Species </th>
    <th align="center"> Precision </th>
    <th align="center"> Recall </th>
    <th align="center"> F1-score </th>
    <th align="center"> Support </th>
    <th align="center"> Interpretation </th>
  </tr>
  <tr>
    <td align="left"> Iris-setosa </td>
    <td align="center"> 1.00 </td>
    <td align="center"> 1.00 </td>
    <td align="center"> 1.00 </td>
    <td align="center"> 10 </td>
    <td align="left"> All the samples are correctly predicted. </td>
  </tr>
  <tr>
    <td align="left"> Iris-versicolor </td>
    <td align="center"> 0.82 </td>
    <td align="center"> 0.90 </td>
    <td align="center"> 0.86 </td>
    <td align="center"> 10 </td>
    <td align="left"> Most predicted as versicolor are correct (82%). Of all versicolor samples, 90% were correctly identified. </td>
  </tr>
  <tr>
    <td align="left"> Iris-virginica </td>
    <td align="center"> 0.89 </td>
    <td align="center"> 0.80 </td>
    <td align="center"> 0.84 </td>
    <td align="center"> 10 </td>
    <td align="left"> Most predicted as virginica are correct (89%). Of all virginica samples, 80% were correctly identified. </td>
  </tr>
</table>


<p><strong>Table 2:</strong> Overall Model Performance Metrics </p>
<table border="1" cellspacing="0" cellpadding="5">
  <tr>
    <th align="left"> Metric </th>
    <th align="center"> Precision </th>
    <th align="center"> Recall </th>
    <th align="center"> F1-score </th>
    <th align="center"> Support </th>
    <th align="center"> Interpretation </th>
  </tr>
  <tr>
    <td align="left"> Accuracy </td>
    <td align="center"> - </td>
    <td align="center"> - </td>
    <td align="center"> 0.90 </td>
    <td align="center"> 30 </td>
    <td align="left"> Overall, 90% of all predictions were correct. </td>
  </tr>
  <tr>
    <td align="left"> Macro Average </td>
    <td align="center"> 0.90 </td>
    <td align="center"> 0.90 </td>
    <td align="center"> 0.90 </td>
    <td align="center"> 30 </td>
    <td align="left"> Simple (unweighted) average of metrics across all classes, which treats all classes equally regardless of their support. </td>
  </tr>
  <tr>
    <td align="left"> Weighted Average </td>
    <td align="center"> 0.90 </td>
    <td align="center"> 0.90 </td>
    <td align="center"> 0.90 </td>
    <td align="center"> 30 </td>
    <td align="left"> Average of metrics weighted by the number of true samples per class. </td>
  </tr>
</table>


<table>
  <tr>
    <td align="center"><img src="https://github.com/ArnabUshna24/CodeAlpha_Iris_Flower_Classification/blob/main/performance_metrics_visualizations/confusion_matrix.png" alt="Confusion Matrix" width="400"/></td>
    <td align="center"><img src="https://github.com/ArnabUshna24/CodeAlpha_Iris_Flower_Classification/blob/main/performance_metrics_visualizations/feature_importance.png" alt="Feature Importance" width="500"/></td>
    <td align="center"><img src="https://github.com/ArnabUshna24/CodeAlpha_Iris_Flower_Classification/blob/main/performance_metrics_visualizations/scatter_plot_petalFeatures.png" alt="Class Cluster for Petal Features" width="400"/></td>
  </tr>
  <tr>
    <td align="left"> Fig. 1: Confusion matrix </td>
    <td align="left"> Fig. 2: Feature importance from Random Forest (RF) </td>
    <td align="left"> Fig. 3: Class cluster for petal features </td>
  </tr>
</table>


If you have any queries, contact me: arnabnushna24@gmail.com
