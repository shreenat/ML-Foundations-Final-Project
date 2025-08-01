# ML Foundations Final Project
This is my final project for the ML Foundations course by Cornell which aims to predict the hours per week an individual works based on Census data. It follows the ML Life Cycle to clean and prepare data and then build, train and evaluate models to find the best one for the Supervised Learning Regression problem.

# Links
- [Jupyter Notebook](https://github.com/shreenat/ML-Foundations-Final-Project/blob/main/DefineAndSolveMLProblem.ipynb)
- Dataset

# Why it is important?
Predicting the hours per week that an individual will invest in their work can help companies make administrative and recruitment decisions. It can also be used to create policies that prevent overworking of employees and provide the necessary resources to families.

# How it was done.
- First I used basic Pandas and Numpy functions to inspect the data for outliers, missing values, column types etc.
- To clean the data, I performed imputation for handling missing values and winsorization for outliers. I normalized all the numeric columns and grouped the open-ended categorical columns. Finally, I used One-Hot-Encoding to convert all the categorical fetaures to numeric ones.
- Using the correlation values of the features with the models, I tested different feature sets for different models using stepwise feature selection.
- I also used model selection to test different model types (KNN, Decision Tree, and Linear Regression and different hyperparameter values (using basic iteration and gridsearch)
- I performed out-sample-validation on testing data to evaluate and compare each model using the Root Mean Squared Error (RMSE) and Coefficient of Determination metrics (r^2). 

# Results
Results of the Best Performing Model: <br>

Test set results <br>
Root mean squared error:  10.429963275398961 <br>
Coefficient of determination(r^2):  0.22973292754561403 <br>
<br>
Training set results<br>
Root mean squared error:  10.224447857714626 <br>
Coefficient of determination(r^2):  0.27025246998329366 <br>

Although, this model performed the best out of all the models trained and tested in the model selection process, the coeeficient of determination(r^2) value is not at all close to 1 and the root mean squared error is also too high. The model is underfitting.


# Roadblocks and Future Improvements
- The models were evaluate by calculating the Root Mean Square Error (RMSE) and the Coefficient of Determination (r^2) for the models on test data to perform out-of-sample validation. However, even for the best performing model derived from the model selection process, the r^2 value was low and the loss value high. This is likely because the data available was limited with the features not correlating well with the label. The future goal would be to build new features that are more relevant to the label.
- The data used here is also from a Census from 1994 which is not applicable today. It would be more useful to get data more recent data and that too from multiple years.




 
