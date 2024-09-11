# Bike Sharing Demand Prediction

[**Dataset Download Link**](https://1024terabox.com/s/1z-q7Rd11gRkT951JWUu4Sw)

### Project Overview:

This project focuses on predicting the demand for shared bikes based on multiple features using **Multiple Linear Regression**. The bike-sharing service provider, BoomBikes, is looking to understand the factors affecting demand to strategize and meet customer expectations in a post-pandemic scenario. The analysis will aid in developing a robust business plan to revitalize revenue streams.

### Problem Statement:

BoomBikes, a US-based bike-sharing company, has faced a dip in revenues due to the COVID-19 pandemic. As the lockdown comes to an end, the company aims to prepare itself to meet the post-pandemic demand by understanding the key factors that influence bike rentals. The goal of the project is to build a multiple linear regression model to predict the demand for shared bikes using historical data and a variety of factors like weather, season, year, and more.

### Dataset:

The dataset includes daily bike rental counts along with various features such as:

- **Season**: Spring, Summer, Fall, Winter
- **Year**: 2018, 2019
- **Month**: January to December
- **Weather**: Clear, Cloudy, Rainy, Snowy
- **Temperature**: Normalized temperature in Celsius
- **Humidity**: Normalized humidity
- **Windspeed**: Normalized windspeed
- **Holiday**: Whether the day is a holiday or not
- **Working Day**: Whether it’s a working day or not
- **Casual**: Number of casual users
- **Registered**: Number of registered users
- **Count (Target Variable)**: Total number of bike rentals (sum of casual and registered users)

The dataset also includes categorical variables (like season and weather), which need to be transformed appropriately before model building.

### Objective:

- To build a linear regression model that identifies the key factors affecting bike demand.
- To determine how well these features predict bike demand (R-squared and adjusted R-squared values).
- To provide insights to BoomBikes for business strategy refinement.

### Approach:

1. **Data Cleaning & Preparation**:
   - Handling missing values, if any.
   - Conversion of numerical categorical variables (like 'season', 'weather', etc.) into actual categorical types (using One-Hot Encoding or Label Encoding).
   - Dropping unnecessary columns that won’t contribute to the model's performance.
   
2. **Exploratory Data Analysis (EDA)**:
   - Univariate and bivariate analysis to understand feature relationships.
   - Visualizing trends across variables such as year, season, weather, and their impact on demand.

3. **Model Building**:
   - Splitting the data into training and testing sets.
   - Building a Multiple Linear Regression model using features as independent variables and the total count of rentals ('cnt') as the dependent variable.
   
4. **Model Evaluation**:
   - Calculating performance metrics like R-squared and adjusted R-squared on both the training and test sets.
   - Residual analysis to check for model assumptions like linearity, homoscedasticity, and normal distribution of errors.

5. **Prediction**:
   - Predicting demand for bikes using the test set.
   - Evaluating the prediction using the R-squared score.

### Requirements:

- **Python** (v3.6+)
- **Jupyter Notebook**
- Libraries used in this project:
  - pandas
  - numpy
  - seaborn
  - matplotlib
  - sklearn (for building and evaluating the linear regression model)

### Files:

- **Jupyter Notebook**: Contains the complete code for the analysis, data preprocessing, model building, and evaluation.
- **Dataset**: The dataset used to train the model, including all the independent variables and target variable (total rentals).
- **Subjective Questions PDF**: A document answering theoretical questions related to multiple linear regression.

### Instructions to Run:

1. Download or clone the repository from [GitHub Link].
2. Open the Jupyter notebook (`bike_sharing_demand_prediction.ipynb`).
3. Run the notebook step by step to see the data preparation, model training, evaluation, and prediction process.
4. Ensure that all the required Python libraries are installed (`pip install -r requirements.txt`).
5. Review the subjective questions PDF for a deeper understanding of multiple linear regression.

### Evaluation Metrics:

- **R-squared**: Indicates how well the independent variables explain the variance in the target variable.
- **Adjusted R-squared**: Adjusted version of R-squared that accounts for the number of predictors in the model.
- **Residual Plot**: Used to check the assumptions of the linear regression model.

### Repository Name Suggestions:

- `bike-demand-prediction`
- `BoomBikes-Demand-Prediction`
- `Bike_Sharing_Linear_Regression_Model`
- `SharedBike-Demand-Forecasting`

### Conclusion:

This project leverages Multiple Linear Regression to predict bike demand based on a variety of factors. The insights from the model will help BoomBikes in making informed business decisions and adjusting their strategy to better cater to post-pandemic demand in the American market.

### Data Dictionary:
=========================================
Dataset characteristics
=========================================	
day.csv have the following fields:
	
	- instant: record index
	- dteday : date
	- season : season (1:spring, 2:summer, 3:fall, 4:winter)
	- yr : year (0: 2018, 1:2019)
	- mnth : month ( 1 to 12)
	- holiday : weather day is a holiday or not (extracted from http://dchr.dc.gov/page/holiday-schedule)
	- weekday : day of the week
	- workingday : if day is neither weekend nor holiday is 1, otherwise is 0.
	+ weathersit : 
		- 1: Clear, Few clouds, Partly cloudy, Partly cloudy
		- 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
		- 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
		- 4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
	- temp : temperature in Celsius
	- atemp: feeling temperature in Celsius
	- hum: humidity
	- windspeed: wind speed
	- casual: count of casual users
	- registered: count of registered users
	- cnt: count of total rental bikes including both casual and registered
	
=========================================
License
=========================================
Use of this dataset in publications must be cited to the following publication:

[1] Fanaee-T, Hadi, and Gama, Joao, "Event labeling combining ensemble detectors and background knowledge", Progress in Artificial Intelligence (2013): pp. 1-15, Springer Berlin Heidelberg, doi:10.1007/s13748-013-0040-3.

@article{
	year={2013},
	issn={2192-6352},
	journal={Progress in Artificial Intelligence},
	doi={10.1007/s13748-013-0040-3},
	title={Event labeling combining ensemble detectors and background knowledge},
	url={http://dx.doi.org/10.1007/s13748-013-0040-3},
	publisher={Springer Berlin Heidelberg},
	keywords={Event labeling; Event detection; Ensemble learning; Background knowledge},
	author={Fanaee-T, Hadi and Gama, Joao},
	pages={1-15}
}

=========================================
Contact
=========================================
	
For further information about this dataset please contact Hadi Fanaee-T (hadi.fanaee@fe.up.pt)
