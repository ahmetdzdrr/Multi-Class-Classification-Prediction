# Multi-Class-Classification-Prediction
A multiple classification prediction has been conducted based on the dataset regarding the acceptability of cars. In the predictions made, various operations have been performed on the class attribute.

Car Acceptability Dataset Overview

Greetings everyone,
In this project, we will perform multi-class classification prediction based on the features present in the given dataset. Below are some key details about the dataset that will be used for this prediction:

The dataset contains approximately 1800 rows. There are a total of 7 columns in the dataset. The target variable in the dataset is labeled as "class". Here is a brief description of each column in the dataset:

Buying

Description: Buying price of the car, categorized into different levels of affordability.

Examples: low, med, high

Maint

Description: Price of the maintenance of the car, categorized into different levels of affordability.

Examples: low, med, high

Doors

Description: Number of doors in the car.

Examples: 2, 3, 4

Persons

Description: Capacity in terms of persons the car can carry.

Examples: 2, 4, more

Lug_boot

Description: The size of the luggage boot in the car.

Examples: small, med, big

Safety

Description: Estimated safety level of the car.

Examples: low, med, high

Class

Description: Car acceptability, categorized into different levels.

Examples: unacc (unacceptable), acc (acceptable), good, v-good (very good)

**************************************************************************************************
**************************************************************************************************

Summary of Data Quality Checks

Shape: The dataset consists of a total of {{num_rows}} rows and {{num_columns}} columns.

Info: The dataset information provides details about the data types, non-null counts, and memory usage.

Types: Data types of each column are displayed to understand the nature of the data.

Missing Values: The count of missing values in each column is shown. There are no missing values in the dataset.

Duplicated Values: The number of duplicated rows in the dataset is presented. There are no duplicated rows.

Unique Values: The count of unique values in each column is displayed, which gives an idea of the cardinality of categorical features.

Describe: Descriptive statistics including mean, standard deviation, minimum, 5th percentile, 25th percentile (Q1), median (50th percentile), 75th percentile (Q3), and 95th percentile are shown for numerical columns.

**************************************************************************************************
**************************************************************************************************

Summary of Unexpected Value Check

The function iterates through each categorical column in the dataset. It checks for values that contain certain special characters such as !, ?, @, and others. These unexpected values might indicate data entry errors or anomalies.

**************************************************************************************************
**************************************************************************************************

Summary of Special Character Replacement and Unexpected Value Check

The replace_special_chars function uses regular expressions to remove certain special characters from the categorical columns in the dataset.

For each column, the function iterates through the DataFrame, applies the special character replacement, and then replaces any empty values with NaN using np.nan.

The unexcepted_value function is then used again to check for any remaining unexpected values in the dataset after the special character replacement.

The function outputs the results for each categorical column

**************************************************************************************************
**************************************************************************************************

Summary of Null Values Visualization

The code calculates the count and percentage of null values in each column of the dataset.

The horizontal bar chart is generated using Matplotlib to visually represent the percentage of null and non-null values for each column.

Columns with missing values are shown in red, while columns with no missing values are shown in orange.

The chart is labeled with titles, axes, and legend for clear understanding.

The function autolabel adds labels to the bars to display the percentage values.

This visualization provides an insightful overview of the distribution of null values in the dataset, aiding in identifying columns with significant missing data.

![__results___14_0](https://github.com/ahmetdzdrr/Multi-Class-Classification-Prediction/assets/117534684/8ed6294b-3254-464d-83a8-850d044a693e)

**************************************************************************************************
**************************************************************************************************

Summary of Count Dataset Features Visualization

The function plot_barplots generates count bar plots for each categorical column in the DataFrame.

The plots are arranged in a grid layout defined by the parameters nrow and ncolumn.

For each column, a count bar plot is created using Seaborn's countplot function.

The title of each plot indicates the column name, and the x-axis represents the categorical values.

The y-axis represents the count of occurrences of each categorical value.

Text labels are added above each bar to display the corresponding count.

The function also handles the layout and display of plots based on the specified grid layout.

![__results___20_0](https://github.com/ahmetdzdrr/Multi-Class-Classification-Prediction/assets/117534684/a0adc867-5145-4e40-b1c3-ad25c0447f2a)

**************************************************************************************************
**************************************************************************************************

Correlation Matrix

![__results___25_0](https://github.com/ahmetdzdrr/Multi-Class-Classification-Prediction/assets/117534684/28676f14-7210-4e0d-9f15-6c32b686d505)

**************************************************************************************************
**************************************************************************************************

Model Training, Evaluation, and Result Visualization

In this section, a function named model is defined to train, evaluate, and visualize the performance of a set of machine learning models. Additionally, another function named model_to_dataframe is provided to summarize the results of the model evaluations in a structured DataFrame.

plot_confusion_matrix Function

This function, plot_confusion_matrix, takes true labels (y_true), predicted labels (y_pred), the model's name (model_name), and an axis (ax) to create and display a confusion matrix heatmap. The confusion matrix visually represents the distribution of correct and incorrect predictions for each class.

model Function

The model function performs the following steps for each model specified in the models dictionary:

Fits the model using the resampled training data (X_train_resampled and y_train_resampled). Generates predictions (y_pred) on the test set. Calculates accuracy, precision, recall, and F1 score using various scoring metrics. Stores the evaluation metrics in the results dictionary. Calls the plot_confusion_matrix function to visualize the confusion matrix for the current model. Finally, it displays a grid of confusion matrix heatmaps for each model using matplotlib and returns the results dictionary containing the evaluation metrics.

model_to_dataframe Function

This function, model_to_dataframe, utilizes the model function to evaluate the models' performance and converts the resulting results dictionary into a structured DataFrame. The DataFrame includes columns for 'Accuracy', 'Precision', 'Recall', and 'F1 Score' for each model.

Confusion Matrix

![__results___31_0](https://github.com/ahmetdzdrr/Multi-Class-Classification-Prediction/assets/117534684/159831e2-ab71-474e-9946-e143ae11ff6a)

**************************************************************************************************
**************************************************************************************************

Summary of Feature Importance Visualization

The function plot_feature_importance is utilized to visualize the importance of features in a machine learning model.

The function accepts a trained model object, a list of feature names, and an optional parameter top_n to specify the number of top features to display.

The function calculates the feature importances from the model and arranges them in descending order.

If top_n is specified, the function selects the top features based on importance scores and their corresponding feature names.

A bar plot is generated using Seaborn's barplot, where the x-axis represents feature importance scores, and the y-axis represents the feature names.

The color palette 'viridis' is used for a visually appealing representation.

The plot is labeled with axes and a title indicating the number of top features displayed.

![__results___36_0](https://github.com/ahmetdzdrr/Multi-Class-Classification-Prediction/assets/117534684/59f2f162-3968-47d4-9841-6baf4e869fee)












