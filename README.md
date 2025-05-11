# MachineLearning_Assignment9-4
Repository for Machine Learning Assignment 9 : Posting Assignment 4

1. Find a classification dataset that you will be able to explain thoroughly in the notebook check. Your features may be indicator variables or quantitative variables. Your label should be categorical (you may have more than 1 category). Create a support vector classifier using radial basis functions for your kernel. Use a grid search to try and determine an optimal value for gamma and C. For the sake of computing time, it is recommended that you do not use a dataset with more than 10,000 entries. You may use a larger dataset, but it is recommended that you perform a random sample of 10,000 rows in this case.

Dataset : 
"weather_forecast_data.csv"
https://www.kaggle.com/datasets/zeeshier/weather-forecast-dataset?select=weather_forecast_data.csv

This dataset is detrermining if there will be either rain or no rain based off of quantatative features such as temperature, humidity, wind spees, cloud coverage, and pressure. I first used a SVC using radial basis functions without any optimal parameters and received a test score of 0.877. After performing a gridsearch and using optimal parameters a test score of 0.971 was received with accuracy of 0.9707.

![Assign4_CM](https://github.com/user-attachments/assets/a5a09a80-e5a7-49ec-9ef7-f1e703cbe124)


2. Product a confusion matrix for the SVC you made in part 2. Our default way to perform grid search is to use the score. Explain why this may not be optimal. Do you think it is optimal in the case of the data you selected?

In my confusion matrix, I decided to use the score, or accuracy. Using the default of score to gridsearch may not be optimal in some cases if the dataset is imbalanced (Much more Yes's than No's). However, for this dataset I believe that in general weather prediction, using the score/accuracy is acceptable as there are minimal consequences of false positives/negatives and great advantages of true positives/negatives.

If this prediction was needed for something along the lines of flash flood/ disaster weather warnings, I would want to maximize my Recall instead of Score (even at the expense of other categories) as missing, or a false negative, on a disaster approaching could have colossal impacts.
