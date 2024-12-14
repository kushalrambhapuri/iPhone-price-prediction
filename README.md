# iPhone Price Prediction
Now you can predict the price of the next iPhone—though it might cost you an arm and a leg—all with just 6 lines of Python code!
I created this prediction tool using PyCharm, a popular Python code editor. Follow the steps below to build your own iPhone price predictor:
Prerequisites
Python Installed: Ensure Python is installed on your system.
Install Pandas: Open the terminal and run the following command:
pip install pandas  
Pandas is essential for handling the data needed to make accurate predictions.
Install scikit-learn: Install the library for machine learning:
pip install scikit-learn  
Code Explanation
Importing Libraries: Start by importing the necessary libraries:

import pandas as pd  
from sklearn.linear_model import LinearRegression  
Load Data: Load your iPhone price data into a Pandas DataFrame:

data = pd.read_csv('iphone_price.csv')  
Ensure you have a CSV file (iphone_price.csv) containing historical iPhone versions and their corresponding prices.

Initialize the Model: Create a LinearRegression model:
model = LinearRegression()  
Train the Model: Fit the model to the dataset using iPhone versions and prices:

model.fit(data[['version']], data[['price']])  
Make Predictions: Predict the price of the next iPhone version (e.g., version 13):

print(model.predict([[13]]))  
Example Output
If your dataset is accurate, the script will output the predicted price for the iPhone version you specify.

Notes
Ensure your iphone_price.csv file is in the same directory as your script and contains columns version and price.
This is a basic example of linear regression for educational purposes. For more accurate predictions, consider adding more features or using advanced models.
And that’s it! Your iPhone price predictor is ready to forecast the cost of the next iPhone.
