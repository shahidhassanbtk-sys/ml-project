# ml-project
Global Temperature Analysis and Prediction (1950–2025)

A data analysis and machine learning project that explores country-level temperature data from 1950 to 2025 and builds a simple model to predict Pakistan's temperature.

Overview

The project covers the full workflow of a small data science task:

Load and inspect the dataset
Clean the data
Explore temperature trends globally and by country
Visualize the results
Train and evaluate a regression model
Dataset
Size: 18,772 rows and 11 columns
Time range: 1950 to 2025 (76 years)
Key columns:
entity: country code (e.g., PAK, IND, USA)
period: the year
value: average temperature in °C
Source: Add your dataset link here

Several columns (lower, upper, interval, note, missing_reason, age_bp) are completely empty and are not used in the analysis.

Tools and Libraries
Python 3
pandas
matplotlib
seaborn
scikit-learn
Jupyter Notebook / Google Colab
Analysis Steps
Data cleaning: converted period and value to numeric types and dropped rows with missing values
Exploration: found the first and last year and the number of years covered; ranked the 10 hottest and 10 coldest countries by average temperature
Global trend: plotted the average global temperature per year
Country comparison: compared Pakistan (PAK), India (IND), and the USA over time with a line chart and a heatmap of the last 20 years
Machine Learning Model
Goal: predict Pakistan's yearly temperature from the year
Model: Linear Regression (scikit-learn)
Split: 80% training (60 years) and 20% testing (16 years), kept in time order (shuffle=False)
Results
Metric	Score
MAE	0.39
MSE	0.19
R²	-0.006

Interpretation: The average error is about 0.39 °C, but the R² score is close to zero, which means the model using only the year performs about the same as predicting the average. Temperature depends on more than the year alone, so a simple linear model is limited here.

Future Improvements
Add features such as rolling averages or lagged temperatures
Try other models (Random Forest, Gradient Boosting, ARIMA, or Prophet)
Extend the prediction to other countries
Forecast future years beyond 2025
How to Run
Clone the repository:
bash
   git clone https://github.com/shahidhassanbtk-sys/ml-project.git
   cd ml-project
Install the libraries:
bash
   pip install pandas matplotlib seaborn scikit-learn jupyter
Open the notebook and run all the cells:
bash
   jupyter notebook
Author

shahidhassanbtk-sys
