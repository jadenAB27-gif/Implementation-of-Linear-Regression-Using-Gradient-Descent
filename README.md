# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries and load the 50_Startups.csv dataset.
2. Extract R&D Spend as the independent variable (X) and Profit as the dependent variable (Y).
3. Initialize the slope, intercept and learning rate, then calculate and update them using Gradient Descent.
4. Predict the profit and plot the actual data points with the regression line.

## Program:
```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

data=pd.read_csv('50_Startups.csv')
X=data['R&D Spend'].values
Y=data['Profit'].values

X=(X-X.mean())/X.std()
Y=(Y-Y.mean())/Y.std()

m=0
b=0
lr=0.01
n=len(X)

for i in range(1000):
    Y_pred=m*X+b
    dm=(-2/n)*np.sum(X*(Y-Y_pred))
    db=(-2/n)*np.sum(Y-Y_pred)
    m=m-lr*dm
    b=b-lr*db

Y_pred=m*X+b

print("Slope:",m)
print("Intercept:",b)

plt.scatter(X,Y,color='blue')
plt.plot(X,Y_pred,color='red')
plt.xlabel("R&D Spend")
plt.ylabel("Profit")
plt.title("Linear Regression using Gradient Descent")
plt.show()

```

## Output:

<img width="1172" height="740" alt="image" src="https://github.com/user-attachments/assets/c2288dd4-3179-4cbe-a782-be1b32cf3783" />
<img width="1162" height="597" alt="image" src="https://github.com/user-attachments/assets/96bb3b74-7ba6-48a3-baf2-797b18354a06" />


## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
