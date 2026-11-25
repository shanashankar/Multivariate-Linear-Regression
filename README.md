# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Import **Pandas** and the required module from **Scikit-learn**.

### Step2
Read the `carsemission.csv` dataset.

### Step3
Select `Weight` and `Volume` as independent variables.
Select `CO2` as the dependent variable.

### Step4
Create and train a Multivariate Linear Regression model

### Step5
Display the regression coefficients and intercept
Display the predicted CO₂ emission.


## Program:
```
Developed by: sahana shankar
Reg number: 26002875

(a)
import pandas as pd

url = "https://raw.githubusercontent.com/arunpradeep-sec/Linear-Algebra-Lab/main/carsemission.csv"

df = pd.read_csv(url)
df.to_csv("carsemission.csv", index=False)

print("Dataset loaded successfully.")
(b)
import pandas as pd
from sklearn import linear_model
df = pd.read_csv("carsemission.csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
input_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})
predictedCO2 = regr.predict(input_data)
print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)







```
## Output:

### Insert your output
<img width="1920" height="1080" alt="Screenshot 2026-11-25 090150" src="https://github.com/user-attachments/assets/f9ac5dc1-4d0c-40d1-bc44-5f1d79528ffc" />

<img width="1920" height="1080" alt="Screenshot 2026-11-25 090307" src="https://github.com/user-attachments/assets/f133e042-50df-44cc-8429-adf36338e0bf" />

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
