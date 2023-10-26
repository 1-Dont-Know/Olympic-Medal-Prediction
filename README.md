# Olympic Medal Prediction

This project uses machine learning to predict the number of medals a country would win in the Olympics based on previous data. The methodology and code were inspired by a tutorial video from Dataquest, which can be found here.

## Libraries Used

- **pandas**: This library was used for data manipulation and analysis. It provided data structures and functions needed to manipulate structured data.

- **numpy**: This library was used for numerical computations. It was particularly used to select numerical data types in the dataset.

- **seaborn**: This library was used for data visualization. It was used to create scatter plots and histograms to visualize the relationships between different variables.

- **sklearn**: This library was used for machine learning. Specifically, the `LinearRegression` model from sklearn was used to train and make predictions on the dataset.

## Methodology

1. **Data Cleaning**: Rows with missing values are dropped from the dataset using pandas.

2. **Data Splitting**: The dataset is split into a training set (teams from years before 2012) and a test set (teams from years 2012 and later) using pandas.

3. **Model Training**: A Linear Regression model from sklearn is trained on the training set, using `athletes` and `prev_medals` as predictors and `medals` as the target variable.

4. **Prediction**: The trained model is used to predict the number of medals for teams in the test set. Predictions less than 0 are set to 0, and all predictions are rounded to the nearest whole number using numpy.

5. **Evaluation**: The Mean Absolute Error (MAE) between the predicted and actual number of medals is calculated using sklearn metrics.

6. **Error Analysis**: The absolute errors are grouped by team to calculate the mean error for each team. This is then divided by the mean number of medals for each team to calculate an error ratio using pandas.

## Results

The Linear Regression model performed well in predicting medal counts for countries that typically win a lot of medals. However, it was less accurate for countries that win fewer medals. This could be due to various factors such as less data available for these countries or other factors not included in the model that significantly impact their performance.

The results, including error ratios and histograms, can be viewed in Jupyter Notebook.
