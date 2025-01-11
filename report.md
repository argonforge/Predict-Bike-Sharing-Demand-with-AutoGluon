# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Allan Valentine

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
All the values had to be > 0 or else kaggle would have rejected them so I had to either remove them or set the negatives to 0.

### What was the top ranked model that performed?
The best performing model was the add features model WeightedEnsemble_L3 with a validation score of 30.4509 and a kaggle score of 0.62738      

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
Datetime was parsed as a datetime feature to obtain information from timestamp.

### How much better did your model preform after adding additional features and why do you think that is?
model perfomed better by 65.2%

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
It perfomes better in terms of perfomrmance compared to the initial submission.
### If you were given more time with this dataset, where do you think you would spend more time?
Given more time I would tweak the hyperparameters and also tune the models for longer to see how they would perform.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
| model                     | hpo                                    | hpo1           | hpo2                                        | score   |
|---------------------------|----------------------------------------|----------------|---------------------------------------------|---------|
| initial                   | default-values                         | default-values | "presets: 'high quality' (auto_stack=True)" | 1.80128 |
| add-features              | default-values                         | default-values | "presets: 'high quality' (auto_stack=True)" | 0.62738 |
| hpo (top-hpo-model: hpo1) | Tree-Based Models: (GBM, XT, XGB & RF) | KNN            | "presets: 'optimize_for_deployment"         | 0.51576 |

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.


![model_train_score.png](img/model_train_score.png)




### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](img/model_test_score.png)

## Summary
-We used the AutoGluon AutoML tool to help predict bike sharing demand.
-AutoGluon helped us quickly create a basic model and then build more complex ones that make decisions on their own.
-The best model we made with AutoGluon worked really well because we first looked at the data carefully and made some smart changes,   but we didn’t tweak the settings too much.
-AutoGluon tried out many different settings and combinations on its own to find the best ones.
-Even though tuning AutoGluon’s settings made our initial model better, it didn’t beat the model where we just made smart data changes without tuning.
-We found that fine-tuning AutoGluon’s settings can be tricky and depends a lot on how much time we have and the specific settings we choose to adjust.

[def]: img/model_train_score.png

