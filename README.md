# Soil-Moisture-Prediction
This Python script uses a Random Forest Regression algorithm to predict temperature, soil moisture, and humidity from March 11, 2023, to March 31, 2023.
# Requirements
This script requires the following Python libraries:
1) numpy
2) pandas
3) sklearn

You can install these libraries using pip or conda.

# Usage
To use this code, you'll need to do the following:
1) Clone this repository to your local machine.
2) Install the necessary dependencies using pip.
3) Update the input file with your data. The input file should include the following columns:
ttime - timestamp in yyyy-mm-dd hh-mi-ss format

pm - particulate matter (1,2,3 is categorised into different sizes)

am - atmospheric moisture

sm - soil moisture

st - soil temperature

lum - luminosity

temp - temperature

humd - humidity

pres - pressure

Run the Soil Moisture Prediction.py script to generate predictions for the period March 11, 2023, to March 31, 2023.
The output file will be generated in the same folder as the input file, named "predicted_values.csv".

# Configuration
You have the ability to modify dates in order to make predictions about the temperature, humidity, and moisture levels for those specific dates
.
# Input Data
The input data file should be a CSV file with the following columns:

Date: A string representing the date in the format YYYY-MM-DD HH-MI-SS.

Particulate Matter: An integer representing the particulate matter level (pm1, pm2, pm3).

Atmospheric Moisture: A float representing the atmospheric moisture.

Soil Moisture: A float representing the soil moisture.

Soil Temperature: A float representing the soil moisture.

Luminosity: A float representing the luminosity level.

Temperature: A float representing the temperature.

Humidity: A float representing the humidity.

Pressure: A float representing the pressure.

# Output Data
The output data file will be a CSV file with the following columns:

1) Temperature Prediction: A float representing the predicted temperature.
2) Soil Moisture Prediction: A float representing the predicted soil moisture.
3) Humidity Prediction: A float representing the predicted humidity.

# Random Forest Regression
Random forest regression is an ensemble learning method for regression that operates by constructing multiple decision trees at training time and outputting the mean or mode of the predictions of the individual trees. Random forest regression can be used to predict a continuous variable such as temperature, soil moisture, and humidity. It has been proven by multiple researches to yield better prediction results compared to other algorithms such as Support Vector Machines (SVM), Linear Regression (LR), etc.

# Report 

We tried Xtreme gradient boosting, support vector machine, relevance vector machine, variance optimized bagging,multiple linear regression and noticed the accuracy did not cross 90%, but random forest regression gave an accuracy of 98%.

We concatted both user data values and then inputed the missing values ( NaN ) as the column values were not the same and to prevent loss of values. Then we scale it down and  on applying the random forest resgression we get the predicted value and then get an accuracy of 98% and test accuracy is 93%.
Now to predict more data for the rest of march , we first find the mean and get the standard deviation with which we randomly generate input values for the next 20 days and predict the soil moisture , humidity and temperature of the soil

# Team Members 

R S Gokul Varun 8778344369
Jaishana Bindhu Priya 8870040108
Raunit Pratik 9931437073
