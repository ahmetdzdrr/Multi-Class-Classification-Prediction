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

https://www.kaggleusercontent.com/kf/140583573/eyJhbGciOiJkaXIiLCJlbmMiOiJBMTI4Q0JDLUhTMjU2In0..oEW6c_gTn7xBqv2-5e7obQ.81frj1bE0KrRRyO7yDrmY9ApLvI68PjAEdbDBbqdsyz6h4xFlVzy42TLbCEErDNgUM9ph0smMx8WupBZJjWAC5Oxh0tNCSmCKArSv210uv_2-y17RMObHi6JLdkJpIqA6FnVABOHI1rNTRJ2ODDL3vNmNdliuPow9YcLX_AqyIlgrt3CAu9HRpNTDsJi53BFZuat8wVpPG-tYTFn36MtAXhlOsf9O1vdo5cZY1IN4yGEgUa64uAMwPreJJl4k4iMRNtQETwO-uxpMgzMFGTK6WVV3ndwX7Xg1nYbAeYnr5RLX6Pcm5V1ljiUZ4W8lZmEUyICCzaKS1lHXhoz5WlJKkrVCI0ZPwqMDMyL-eUUYUg4TIiz3y2I_cRwolll93Gmuzy6jzZwvyHUnbvHHANaQH7tsSzWrgiqEiaGK86lzD5MTdM0mvdO-iHRSPQ7sN-CG8PPkSBSngzb7LyWPKkC-lRjUDgWQ4HinTWFz-cj4WGVIxgZ2CFHYOtpudr2bEWz45kHKMnC3qSEiMMcKv0exTiDnf2SHer4KxpX7yHe4jAmd1qR9_Q-_1sT6J0NLRyeVZ1Ju4msIh9EO1qYVfMBNFaO6e3q0-6wfx9SEfeXxB7W7CimGmNqDMZxudSrqXMtiVNMPCa7YURQnAqXK7tjqn4ZIOceSh76HOCoAWGgDyme9YYax_hTqWUXnwAibd5D.xNq51_8XgbW3tXoXEzNYew/__results___files/__results___14_0.png

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

https://www.kaggleusercontent.com/kf/140583573/eyJhbGciOiJkaXIiLCJlbmMiOiJBMTI4Q0JDLUhTMjU2In0..ci0rr0jGil0NFh_ilorzkA.8vf71IxTax30c3wbuHawcI7wplfMx4JiP9eB_48I-lYg0BBAysPADoekkaTjXY4C4VSGSh47hVr-XxMmdHPawwd4Mpd3sYHcg6a_BYvwgfrWlUKXjcT2sVohYRIWunx9rAgpGzhi1Pl6V7xotlSGtBr1bBTwdJiDU2dm8--BLOOSA-09hu5ndKMc7gKZya93XrUnwYRJRxCUdlzBr5Tnk5n-nAsl9_AZrTiQ8JE69BWkhXY6m9akcK6-Hmgq8F7TYYJUtYHHpoF27LqOjxCEv51WzyXcKivhEZ6feS1ImP6ZyrZBWawzPWGORhA3Jn_WRBit95a3RG000ev2iBM0DroVVEu_VH_TXD-QszV_p84KlLoBJUTU4QvwblcwZZ58tmQzEF3IVU3RHj2ZCWkz0CQqcEb3xf2jjTg8S_SH4ZYx-DgtmoocLIqY0_8ugfQqBYxVxM6gjhB-s6lrSyG_updcxomIm4w6Zl-8nhjSFbv2ussIdF8U3tHT4anwx4Xw02IcgAfZZ6vexpgIQzfDQqx4ZBnwBVa5NihzNUXBRNl74LcqJsBtu-GSOM_4Xcc-pxK48ZrE3TQb9bUNh3kMU6nczKdFsWm5YbIbU2-hOs-e-TQksdVinMeR-s9m4V7Q1ddUUfQ72E3JPnC-pAffFlRqQlf3DZPPCkkY4uB_i-9MFhoW1k7KSzLXEUO6x0zE.zq4wYOHbUcRcJTfSbKepxg/__results___files/__results___20_0.png

**************************************************************************************************
**************************************************************************************************

Correlation Matrix


