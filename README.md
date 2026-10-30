# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1. Import the required libraries and initialize the input data (Population and Profit).
2. Initialize the slope, intercept, learning rate and number of iterations.
3. Calculate the predicted values and update the slope and intercept using Gradient Descent.
4. Predict the profit and plot the actual data along with the regression line. 

## Program:
```

Program to implement the linear regression using gradient descent.
Developed by: Jaden Samuel Abraham
RegisterNumber: 212225040138

import numpy as np
import matplotlib.pyplot as plt

X=np.array([6,8,10,12,14,16,18,20])
Y=np.array([17,20,25,28,30,35,40,45])

m=0
b=0
lr=0.001
n=len(X)

for i in range(1000):
    Y_pred=m*X+b
    dm=(-2/n)*np.sum(X*(Y-Y_pred))
    db=(-2/n)*np.sum(Y-Y_pred)
    m=m-lr*dm
    b=b-lr*db

print("Slope:",m)
print("Intercept:",b)

Y_pred=m*X+b

plt.scatter(X,Y,color='blue')
plt.plot(X,Y_pred,color='red')
plt.xlabel("Population")
plt.ylabel("Profit")
plt.title("Linear Regression using Gradient Descent")
plt.show()

```

## Output:

<img width="1787" height="641" alt="image" src="https://github.com/user-attachments/assets/141789d2-5a14-45ad-9019-bd1fb276a17b" />
<img width="1235" height="621" alt="image" src="https://github.com/user-attachments/assets/f51d314b-766a-448b-9e79-978f3abc758c" />

## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
