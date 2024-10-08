# Classification Model for Breast Tumor

## Introduction
Breast cancer is the most prevalent cancer among women and there are over 2.3 million recorded patients annually. Early detection of the tumor is critical to improve the success of treatment and minimize the chances of complications. Machine learning algorithms can be instrumental for this purpose by offering sophisticated methods for analyzing complex medical statistics to generate precise predictions for tumor classification. This project utilizes such techniques to create effective models that can differentiate tumors based on biopsy features. The approach involves examining multiple variables, exploring various models and evaluating the performance to enhance diagnostic accuracy and facilitate timely intervention.

## Dataset
The dataset used for this project is the Breast Cancer Diagnostic which can be found in Machine Learning Repository. It consists of 569 instances of patients with tumor and 30 features of various cellular attributes. All of the variables are numerical. These include radius (mean, standard error, worst), texture (mean, standard error, worst), perimeter (mean, standard error, worst), area (mean, standard error, worst), smoothness (mean, standard error, worst), compactness (mean, standard error, worst), concavity (mean, standard error, worst), concave points (mean, standard error, worst), symmetry (mean, standard error, worst), and fractal dimension (mean, standard error, worst). The target variable classifies tumors as M for malignant or B for benign.

## Exploration

<p align="center"><img src="https://github.com/user-attachments/assets/9bb32a21-00a1-43ed-bfc0-0c96bd66badc" alt="1" style="width: 800px; height: 500px;"></p>

The diagram above displays the missing values across individual features. Missing values can give misleading results and should be treated before training models. There are no missing values in this dataset so further treatment is not required in this matter.

<p align="center"><img src="https://github.com/user-attachments/assets/ba7b2460-88d0-4c29-98e7-71e167d6acb3" alt="2" style="width: 800px; height: 500px;"></p>

The diagram above displays the outliers values within individual features. Outlier values can cause biased prediction and must be removed before training models. There are excess amount of outliers in standard error and omitting those features is the correct decision.

<p align="center"><img src="https://github.com/user-attachments/assets/5799662b-b164-472e-9dce-64924f00f673" alt="3" style="width: 800px; height: 500px;"></p>

The diagram above displays the distribution of various tumor cases. This helps to visualize the skewness in dataset by counting the number of positive and negative cases. There are twice as many benign cases compared to malignant cases which will tilt the model.

<p align="center"><img src="https://github.com/user-attachments/assets/477bcc39-e158-4f62-90bb-a814335007ca" alt="4" style="width: 800px; height: 500px;"></p>

The diagram above displays the feature distribution of target variable. Difference in the distribution of the target variables can help the model better at distinction. All the mean of the features show significant variance which can lead to better prediction.

<p align="center"><img src="https://github.com/user-attachments/assets/fc65a59b-f211-40e3-bfba-cf131562d8e9" alt="5" style="width: 800px; height: 500px;"></p>

The diagram above displays the correlation between the various features. Features with strong relation can cause overfitting  and this can be fixed during feature selection. The radius of the tumor has a high positive correlation with the area of the tumor.

## Modeling

<p align="center"><img src="https://github.com/user-attachments/assets/f39c3200-b0ad-469d-a170-6dd75569e2ce" alt="6" style="width: 800px; height: 500px;"></p>

The diagram above represents the confusion matrix for individual models. This helps to visualize the number of accurate predictions and incorrect predictions. All the models are performing outstanding because the number of false positive and false negative is insignificant.

<p align="center"><img src="https://github.com/user-attachments/assets/c385b4ca-e287-42c8-a3a6-b5ceb3283a80" alt="7" style="width: 800px; height: 500px;"></p>

The diagram above represents the performance metrics of the individual models. Sensitivity measures the true positives rate and specificity measures the true negatives rate. It is more important to avoid false negative than false positive since it can dismiss required treatment.

<p align="center"><img src="https://github.com/user-attachments/assets/ae0a9fee-083b-4eff-bcd2-4de18536b7be" alt="8" style="width: 800px; height: 500px;"></p>

The diagram above represents the prediction accuracy of the individual models. This is an overall measure of the capability of the models in distinguishing between benign and malignant. The decision tree seems to be performing the best in this metric.

<p align="center"><img src="https://github.com/user-attachments/assets/fb50ecae-b7f6-45a6-8583-24e3cd9ed652" alt="9" style="width: 800px; height: 500px;"></p>

The diagram above represents the receiver operating characteristic of models. This checks the preciseness of the model and is a better overall measure since there is a class imbalance. The decision tree seems to be performing the best in this metric.

<p align="center"><img src="https://github.com/user-attachments/assets/dced89d9-812d-4427-a4fd-5502b9a62ffc" alt="10" style="width: 800px; height: 500px;"></p>

The diagram above represents the feature importance of optimum model. The shap analysis ranks the features according to their significance in the final result. It shows that some features like concavity has high positive impact and features like texture has high negative impact.

## Conclusion

The project demonstrates the effectiveness of machine learning model in classifying breast tumor using features from biopsy. All the models performed exceptional with the decision tree performing the best in distinguishing between benign and malignant. The results can be improved by utilizing bigger dataset, reducing feature skewness and performing hyperparameter tuning which can improve the predictions capability of the model. Future work could focus on incorporating additional datasets to improve model generalization and exploring advanced techniques like deep learning for further enhancement. Additionally, implementing real-time prediction systems and integrating these models into clinical workflows could assist in early tumor detection and treatment planning.
