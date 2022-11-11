# Machine Learning
 steps to follow
 1. import the required packages
   - load the dataset from sklearn.datasets import load_boston
   - data = load_boston() to load the data to the data variable
   - data.keys() gives the columns/ features in the dataset
   - data.describe() shows the description of the dataset
   - data.target gives the data of dependent variable
 2. preparing the dataset
   - converting the data into dataframe by pd.DataFrame()
   - checking the data with head() and tail() 
   - adding a new column to the dataframe with dataFrame['column_name'] = dataset.target
   - dataframe.info() gives the insights about the datatypes
   - using describe()
   - checking the missing value by using isnull().sum() if any
 3. EDA
   - finding the correlation to understand it better relationship between the features by using .corr()
   - try to visualize the correlation with a heatmap or pairplot
   - ploting with scatter plot to check how much the features are correlated to each other by taking two variables
   - we can also use regplot which is created specially for regression problems
   - assigning the dependent and independent(1 or more) features to the variables
   - divide the data to training and testing data by using train,test and split function fromsklearn by giving test_size of 30%,40%,70% and random state to 42(?)
   - standardize the dataset by using sklearn.preprocessing from StandardScaler
   - scaler.fit_transform the training features and transform testing data
 4. model training
   - from sklearn import LinearRegression() model
   - fit the regression model to the training data of X and Y
   - find the coeffiecient(coeff_) and the intercept_
   - prediction with the test data
   - plot the scatter plot for prediction of two related features(test data,predicted data)
   - calculating the residual(error) in the test-predicted data
   - plot the residuals with seaborn displot of kind "kde" should be normal distribution
   - another scatter plot for predictions and residuals
   - (performance metrics)finding the errors by (y_test,predicted value)mse,mae from sklearn.metrics and rmse
   - find the r squared and adjested r squared
