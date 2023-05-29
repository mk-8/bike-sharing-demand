# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Meet Kavathiya

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
I was mandated to use the.predict method rather than the.evaluate approach throughout the lesson. This resulted in the creation of a pandas series object that acted simply a list of values. This list of values has to be included as a new count column in my submit dataframe. The submitted dataframe was then converted to a csv file, which I then sent to Kaggle.

### What was the top ranked model that performed?
In my case the top ranked model is WeightedEnsemble_L3 with the score_val of 21.529233

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
EDA displayed a breakdown of values, which assisted me in determining which columns included just category data and which, like the minute and second columns I added, were irrelevant. I constructed year, month, day, hour, minute, and second columns off the datetime column for both the train dataset and the test dataset after converting the datetime column to a pandas datetime column type.

### How much better did your model preform after adding additional features and why do you think that is?
Initially i was getting the 2.11138. After Hper parameter optimzation i got 0.51556
## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
I gave tuning a second try and initially saw an improvement of roughly 0.07. I gave it another attempt, but I only saw a 0.03 improvement.

### If you were given more time with this dataset, where do you think you would spend more time?
I might give a try to the feature engineering or fine tuning the model.
### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|120|None|False|2.11138|
|add_features|120|None|False|0.63169|
|hpo|300|3.0|True|0.51556|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](/bike-sharing-demand-1/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.
![model_test_score.png](/bike-sharing-demand-1/model_test_score.png)

## Summary
The project began with Kaggle and Sagemaker setups then after visualized the data and trained the models.
