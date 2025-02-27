# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Divya R V
RegisterNumber: 212223100005 
```
```
import numpy as np
import matplotlib.pyplot as plt

x=np.array(eval(input()))
y=np.array(eval(input()))

xmean=np.mean(x)
ymean=np.mean(y)

num=0
den=0

for i in range(len(x)):
    num=num+(x[i]-xmean)*(y[i]-ymean)
    den=den+(x[i]-xmean)**2

m=num/den

c=ymean-(m*(xmean))

print(m,c)

y_predicted= m*x + c  
print(y_predicted)

plt.scatter(x,y)
plt.plot(x,y_predicted,color='red')
plt.show()
```

## Output:
![best fit line](sam.png)

![Screenshot 2025-02-27 170602](https://github.com/user-attachments/assets/f0cfd3fd-17c9-4183-be3b-1df5aed418f4)

## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
