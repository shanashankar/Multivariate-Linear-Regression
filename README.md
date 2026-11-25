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
Select `CO2` as the dependent variable

### Step4
Create and train a Multivariate Linear Regression model
Display the regression coefficients and intercept
### Step5
Predict the CO₂ emission for:
   - **Weight = 3300**
   - **Volume = 1300**
Display the predicted CO₂ emission.


## Program:
```
[a]
'''developed by: sahana shankar
register number:26002875'''

import pandas as pd

url = "https://raw.githubusercontent.com/arunpradeep-sec/Linear-Algebra-Lab/main/carsemission.csv"

df = pd.read_csv(url)
df.to_csv("carsemission.csv", index=False)

print("Dataset loaded successfully.")
[b]
'''developed by: sahana shankar
register number: 26002875'''

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
<img width="1920" height="1080" alt="Screenshot 2026-11-25 090150" src="https://github.com/user-attachments/assets/c88a308c-56a1-4797-9cfb-3dfe96cac16c" />
<img width="1920" height="1080" alt="Screenshot 2026-11-25 090307" src="https://github.com/user-attachments/assets/2002de36-5211-4120-a15d-22afb7adc470" />



## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
