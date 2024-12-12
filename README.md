README for FinalExam-Nev-Simmons.R


Requirements

R Libraries:

tidyverse: Data manipulation and visualization
caret: Machine learning and model evaluation
knitr: Report generation
patchwork: Plot layout management

Files:

Final Exam.RMD
Description: Contains all of the code for Parts 1,2,3

FinalExam.Rproj 
Description: Contains the project for this problem

diabetes_data.csv
Description: The dataset containing information on diabetes predictors and outcomes.

FinalExam-Dashboard.png
Description: A comprehensive visualization layout of key predictors and their relationships to diabetes.
My Final Dashboard for Part 3 of this assignment.

BoxWhiskerPlot.png
Description: Summarizes model accuracy for training data. Goes with Part 2 of the assignment.

Summary:

This project involves building and evaluating predictive models for diabetes using a dataset of health-related 
predictors. The analysis includes logistic regression, a single regression tree, and a random forest model, 
with 5-fold cross-validation repeated 10 times to assess performance. Variable importance analysis 
identifies HbA1c levels, blood glucose levels, and age as key predictors. While the random forest 
model performs best on training data, it overfits and underperforms on the test set compared to simpler 
models. Visualizations, including violin and density plots, explore relationships between key predictors 
and diabetes outcomes, highlighting HbA1c's strong predictive value as well as age's. The project 
emphasizes balancing model complexity and accuracy in medical predictions.

Solutions: 

Part 1: 

Based on the variable importance of the random forest model, the HbA1c level seems to be the 
most important predictor of diabetes with a score of 91.94. Blood glucose level seems to be 
the next highest predictor of diabetes with a score of 58.7. The next three highest variables 
are age with a score of 41.06, positive for hypertension or high blood pressure with 18.51 and 
lastly positive for heart disease with 13.56. As far as the models are concerned, I chose a 
logistic regression to get a relatively simple model to predict every variable. This gave me 
a good baseline as it is the least complex model chosen. Next I chose a single regression tree 
to get a little more complex but this time only test a small subset of variables. For the variables 
chosen I picked variables I would think would have the most importance in determining diabetes based 
on information learned in biology and prior knowledge of diabetes. Finally I took the most complex 
route of random forest to discover the variable importance as well as get a final baseline using the 
most complex prediction. I chose all predictors to understand the importance of every single predictor 
rather than just a small subset. 

Part 2:

Since Diabetes was changed to a factored variable, we are no longer treating it 
with a continuous response variable. Now this variable is a factored variable
that denotes either 1 or 0 and nothing in between. Based on our Accuracy values which
shows the amount of agreement with the models predictions, we can find that in the
training set the random forest tree although overlapping, seems to be the best 
at predicting the diabetes response variable based on using all of the predictors available.
However, using the test set, the accuracy variable shows that the random forest was 
the worst performing method compared to the other two, and the regression tree was the
best at prediction. This is most likely due to the overfitting that occurs when
using every single predictor rather than using just four in the regression tree.
The problem with this comparison is that one of the models "tree", is using less predictors
and this shows to be just slightly better at prediction rather than the simple logistic 
regression model, most likely due to the less amount of predictors and the more
concise predictors chosen. There is also a lot of error when considering these models,
with the over-lappage of these plots it may be hard to completely trust these results. 
A precision test could be useful here as it would tell us how many false positives
are predicted by the results. Based on the value, we could determine if the true
prediction test is worth using to predict Diabetes, as false positives are a big
no-no in the medical field.
