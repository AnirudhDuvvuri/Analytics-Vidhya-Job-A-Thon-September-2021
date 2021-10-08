# Analytics-Vidhya-Job-A-Thon-September-2021
ML Hackathon - Prediction of Sales for a chain of stores for the next 2 months

Rank : 59 of 6828 participants 

Overview of Approach: 
1. Check the dependencies of variables with target variable by visualizing the data. 
2. Treat any missing values and outliners. 
3. Use sklearn and train the model with different decision tree estimators. 
4. Choose the best estimator for final prediction. 
5. Revert back changes made for treating outliners. 
6. Inspiration for creating approaches is taken from StackOverflow and GeekforGeeks. 

Tools Used: 
Python 3.9 Jupyter Notebook 
Pandas, Numpy and Seaborn modules 
Sklearn decision tree estimators 

Detailed Approach: 

a. Data Import: 
1. Import Train and Test dataframes 
2. Check the columns, datatypes and shapes of dataframes. 
3. Split Date into Month and Dayofweek to get insights into historical trends. 
4. Remove unnecessary columns from Test and Train dataframes. 

b. Data Visualization: 
1. Target data Sales in numerical feature. Use distplot to visualize the data. 
2. Holiday, Discount are Categorial features. 
3. Store_id, Store_Type, Location_Type, Region_Code, Month, Dayofweek are Ordinal features. 
4. Use Seaborn barplot to visualize both categorial and ordinal features. 
5. Use Searborn heatmap to visualize the correlation between different parameters. 

c. Missing value and Outliner Treatment: 
1. Check for missing values in both the datasets. 
2. Since there are no missing values there is no need for imputation. 
3. Use numpy logarithmic function to treat outliners in target variable and delete original column. 
4. Impute infinity values with zero. 

Modelling: 

a. Sklearn basic steps. 
1. Move the target variable to separate dataframe. 
2. Use pd.get_dummies to convert categorial variables into dummy variables i.e series of 0 and 1. 

b. Decision Tree Modelling 
1. Use train_test_split on dataframes. 
2. Train model using below decision tree estimators. 
   LinearRegression 
   Linear_Model.Ridge 
   Linear_Model.Lasso 
   DecisionTreeRegressor 
   RandomForestRegressor 
   XGBRegressor 
3. The best score is from RandomForestRegressor. 
4. Use it to make final prediction in test file. 

Submission File Export: 
1. Import sample submission file. 
2. The target variable was converted to logarithmic format. Use np.exp to revert back logarithmic data. 
3. Create final submission file matching the sample submission file. 
4. Export final submission file in csv format.
