# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 02/05/26

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
```
# Step 1: Import libraries
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression

# Step 2: Load dataset
data = pd.read_csv('/content/salary_prediction_data.csv')

# Step 3: Select feature and target
X = data[['Experience']]    # input
y = data['Salary']          # output

# Step 4: Split dataset
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

# Step 5: Train model
model = LinearRegression()
model.fit(X_train, y_train)

# Step 6: Predict
y_pred = model.predict(X_test)

# Step 7: Plot graph
plt.figure()

plt.scatter(X_test, y_test)     # actual data
plt.plot(X_test, y_pred)        # prediction line

plt.xlabel("Experience")
plt.ylabel("Salary")
plt.title("Salary Prediction Graph")

plt.show()
```
# OUTPUT:


<img width="750" height="566" alt="Screenshot 2026-04-28 093555" src="https://github.com/user-attachments/assets/8089216d-85ce-4e51-9836-f8419b94ecc3" />




# RESULT:
Thus we have created the python code for plotting the time series of given data.
