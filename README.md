# Rent-Prediction
A machine learning model that predicts rents. It takes the required user inputs to predict rent.

# Project Outline
- All libraries imported
- Clean the dataset
- Exploratory Data Analysis
- Data Preprocessing for Model Building
  - Removing outliers
  - Encoding Categorical variables
  - Check for multicollinearity issues
- Building the model
  - Linear Regression Model
  - Model Communication(Linear Regression))
  - Non-Linear Regression Model
    - RandomForestRegressor model
    - Model Communication (RandomForestRegressor))
- Findings
- Model Deployment

# Clean the dataset
- Checked for the data structure to identify incosistencies in the data. It showed that the data structure was okay except for two variables (Longitude and Latitude) which had 719 missing values. Also, the longitude and latitude point to a location but we already have a location variable so those variables were removed.
- Checked for white spaces in the variable names but was clean.
- Checked for duplicates but there wasn't any.

# Exploratory Data Analysis
- Showed the trend of rent prices over posting time.
- Showed the distribution of the property types in the data to which property type the data contain most.
- Plotted the correlation matrix to show the correlation between the variables and also to identify multicollinearity issues.
- Showed the distribution of the furnishing status to know which status dorminates.
- Showed the distribution the age of listing by property type and remove outliers if any.
- Removed all property types that has age equal or more than 1000 days and plot the new distrinbution since those were the outliers.
- Showed the distribution of rents by property type to show the order of rent prices by property types.
- showed the distribution of rents by property type to show the order of rent prices by city.

# Data Preprocessing
- showed the number of unique values in each column in the dataset to check for low and high cardinalities. The Purpose and Frequency variables had low cardinality so they were removed.
- location variable have too many categories so a function was created to shorten the categories.
- Checked for outliers in the Rent variable by Property type, which three values were identified as outliers so they were removed.
