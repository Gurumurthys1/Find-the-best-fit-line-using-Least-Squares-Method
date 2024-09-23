# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
step 1. Get the independent variable X and dependent variable Y.

step 2. Calculate the mean of the X -values and the mean of the Y -values.

step 3. Find the slope m of the line of best fit using the formula. 

<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">

step 4. Compute the y -intercept of the line by using the formula:

<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">

step 5. Use the slope m and the y -intercept to form the equation of the line.

step 6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: GURUMURTHY S
RegisterNumber:  212223230066
*/
import numpy as np
import matplotlib.pyplot as plt
x = np.array(eval(input()))
y = np.array(eval(input()))
x_mean = np.mean(x)
y_mean = np.mean(y)
num = 0
denom = 0
for i in range(len(x)):
    num+=(x[i] - x_mean)*(y[i]-y_mean)
    denom += (x[i]-x_mean)**2
m = num/denom
b = y_mean-m*x_mean
print("m value is ",m,"\nb value is ",b)
y_predicted = m*x+b
print("y predicted value ",y_predicted)
plt.scatter(x,y)
plt.plot(x,y_predicted,color="red")
plt.show()

```

## Output:
![image](https://github.com/user-attachments/assets/46c16be2-c196-47e2-853f-055c89d43ca4)
![image](https://github.com/user-attachments/assets/6d4af5a9-3cfa-4560-89f3-44f6a0699be0)
![image](https://github.com/user-attachments/assets/c9b05228-e79b-4c56-b2e3-6e1d37d3e11b)
![image](https://github.com/user-attachments/assets/af9c9e34-fc73-4188-bd67-76e72849c61d)




## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
