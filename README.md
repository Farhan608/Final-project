Overview

Building a regression model to predict financial indicators is a multi-step process that starts with data preprocessing to ensure quality and consistency. Exploratory data analysis (EDA) follows, providing insights and identifying patterns that can influence the model's performance. The core of the project is the model-building phase, where various regression techniques can be applied to find the best fit for the data. Finally, evaluating the model's accuracy and reliability is crucial to ensure it can make reliable predictions about future financial trends based on historical data.
Dataset


The dataset contains the following columns:
•	date: Date of the record.
•	ISE, ISE.1: Istanbul Stock Exchange indices.
•	SP: S&P 500 index.
•	DAX: German Stock Index.
•	FTSE: Financial Times Stock Exchange Index.
•	NIKKEI: Nikkei Index (Japan).
•	BOVESPA: Brazilian Stock Index.
•	EU: European Union Index.
•	EM: Emerging Markets Index.


Purpose
The purpose of this project is to:
1.	Analyze the relationships between different financial indicators.
2.	Build a regression model to predict one of the indices (ISE or ISE.1) based on the others.
3.	Evaluate the model's performance using various metrics.

   
Structure of the Code
1.	Import Libraries:
o	The project uses libraries like pandas, matplotlib, seaborn, and scikit-learn.
2.	Data Loading:
o	The dataset is loaded using pandas.read_csv().
3.	Data Exploration:
o	Check for missing values using dataset.isna().sum().
o	Basic information about the dataset is printed using dataset.info().
4.	Data Visualization:
o	Pair Plot: sns.pairplot(dataset) is used to visualize the relationships between variables.
o	Line plot: plt.title('Line Plot of ISE and SP') label='SP') to plot Line plots for ISE and SP Indexs
o	Scatter plot: plt.title('Scatter Plot of EM vs NIKKEI') is used to show the scatter plots of two indexs EM and Nikkei
o	Histogram: plt.title('Histogram of FTSE') is used to plot histogram for index FTSE
o	Heatmap: sns.heatmap(dataset.corr(), annot=True) is used to show the correlation matrix.
5.	Model Building:
o	Split the data into training and testing sets using train_test_split for linear regression
o	Build a Linear Regression, Random Forest and LSTM models.
o	Evaluate the models using metrics like mean_squared_error, mean_absolute_error, and r2_score.

Input and Output
•	Input: The input is a CSV file containing financial indices data.
•	Output: The output includes:
o	Visualization plots (line, scatter, histogram, pair plots and heatmap and model performance).
o	Regression model's, Random forest and LSTM evaluation metrics.
Function Descriptions
train_test_split()
•	Purpose: Splits the dataset into training and testing sets.
•	Parameters:
o	test_size: Fraction of the dataset to be used for testing.
o	random_state: Seed for random number generation.
LinearRegression()
•	Purpose: Builds a linear regression model.
•	Parameters: No parameters required for basic usage.
mean_squared_error(), mean_absolute_error(), r2_score()
•	Purpose: Evaluate the regression model's performance.
•	Parameters:
o	y_true: True values of the target variable.
o	y_pred: Predicted values from the model.

How to Run the Project
1.	Ensure all required libraries are installed: pandas, matplotlib, seaborn, scikit-learn.
2.	Load the notebook and run the cells sequentially.
3.	The visualizations and model’s evaluation metrics will be displayed as output.

