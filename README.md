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
- Encoded the categorical variables.
- Checked for multicollineariy issues after the shortening of the categories in the Location variable.

# Building the model
- Built a linear and a non-linear regression models to select the best model that gives us the least error.

# Findings
***Findings from the Exploratory Data Analysis***
- The visualization of the rent posting over time shows an upward trend in rent, and highlights the fluctuation of rents over time, indicating the instability of rent over time.
- The data also highlights that most of the property types in the data are apartment, followed by villa and the other types in descending order of counts, with residential plots holding the least counts.
- The correlation matrix highlights very low correlations between each of the independent variables and the rent, the target variable, with the exception of the number of beds variable which has a low correlation(**0.31**) with the rent variable.
- The matrix also does not show any multicollinearity issues since the correlations between the independent variables are not very strong.
- The analysis shows that rent prices are higher in Dubai, followed by Abu Dhabi, Sharjah, Ajman, Al Ain,Ras Al Khaimah, Umm Al Quwain and Fujairah. It shows that Fujairah has the least rent price.

***2. Findings from the model***
**Our multiple linear equation shows that:**
- a unit increase in the number of beds is associated with an increase in rent by ***GHC222138.81***,  h olding other variables constant.
- a unit increase in the number of furnishing is associated with a decrease in rent by ***GHC99609.89***,  holding other variables constant.
- a unit increase in the number of property type is associated with an increase in rent by ***GHC11486.54***, holding other variables constant.
- a unit increase in the size of the rent per square feet is associated with an increase rent by ***GHC43.13***, holding other variables constant.
- a unit increase in the age(days) of the listing is associated with an increase in the rent by ***GHC5067.76***, holding other variables constant.
- a unit increase in the age(days) of the number of locations is associated with a decrease in the rent by ***GHC121567.34***, holding other variables constant.
- a unit increase in the a𝑟𝑒𝑎 (𝑖𝑛 𝑠𝑞𝑓) of the property is associated with an increase in the rent by ***GHC13015.86***, holding other variables constant.
- a unit increase in the number of the cities is associated with an increase in the rent by ***GHC81.65***, holding other variables constant.
- a unit increase in the number of bathrooms is associated with an increase in the rent by ***GHC59.7***, holding other variables constant.
- an additional unit in rent category is associated with a decrease in the rent by ***GHC9633.54***, holding other variables constant.
      - The model gives a mean absolute error of ***162969.44***, which is very high when compared to the RandomForestRegressor model


***3. Finding from the RandomForestRegressor model***
 - The model gives us a mean absolute error of ***4309.64*** which is the lowest error when compared to the Linear Regression model.
 - The general contribution of each feature from the model, according to the model communication, shows that the rent category is the best contributor to the model followed by the rent per squared feet and the others in the descending order, with the furnishing status variable being the least contributor to the model.
