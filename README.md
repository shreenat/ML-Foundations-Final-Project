# ML Foundations Final Project
This is my final project for the ML Foundations course by Cornell which aims to predict the hours per week an individual works based on Census data. It follows the ML Life Cycle to clean and prepare data and then build, train and evaluate models to find the best one for the Supervised Learning Regression problem.

# Links
- [Jupyter Notebook](https://github.com/shreenat/ML-Foundations-Final-Project/blob/main/DefineAndSolveMLProblem.ipynb)
- [Dataset](https://github.com/shreenat/ML-Foundations-Final-Project/blob/main/censusData.csv)

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

# How to test the code?
1. Install Jupyter Notebooks
If you don't already have Jupyter notebooks installed on you device, follow the instructions at the following link to install it : <br>
https://jupyter.org/install

2. Download the Jupyter Notebook
  Download the Jupyter Notebook for whichever lab you want to run.

2. Launch Jupyter Notebooks Server
- Open your terminal or command prompt.
- Navigate to the directory where you want to store or access your Jupyter notebooks using the cd command (e.g., cd Documents/MyNotebooks).
- Type the following command and press Enter: <br>
 ``` jupyter notebook ```

3. Open the Notebook in Jupyter Notebooks Server
- Navigate to the .ipynb file in the Jupyter Notebook interface and click on its name

4. Upload the sample dataset
- Download the dataset file.
- In the top-right corner of the Jupyter Notebook dashboard, locate and click the "Upload" button. This action will open a file selection dialog from your local machine.
- Select the dataset file from your local file system.
  
6. Interact with the Notebook:
- Cells: Jupyter notebooks are composed of cells. You can have code cells (where you write and execute code) and Markdown cells (for text, explanations, and formatting).
- Running Cells:To execute a code cell, select the cell and press Shift + Enter, or click the "Run" button in the toolbar. The output of the code will appear directly below the cell.
- Saving: Notebooks are automatically saved periodically, but you can also manually save them by clicking the "Save" icon or going to "File" > "Save and Checkpoint."

6. Shut Down the Server:
To stop the Jupyter Notebook server, go back to your terminal or command prompt where the server is running.
Press Ctrl + C twice to shut down the server and all associated kernels.



 
