# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Start the Program
2. Use numpy and sys packages
3. Use nested loops to loop through each row and column
4. End the program


## Program:
```

Program to find the solution of a matrix using Gaussian Elimination.
Developed by: KEERTHIVASAN M
RegisterNumber: 212223100021

import numpy as np
import sys
n=int(input())
matrix=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        matrix[i][j]=int(input())
for i in range(n):
    if matrix[i][j]==0.0:
        sys.exit("Divide by zero error")
    for j in  range(i+1,n):
        ratio=matrix[j][i]/matrix[i][i]
        for k in range(n+1):
            matrix[j][k]=matrix[j][k]-ratio*matrix[i][k]
x[n-1]=matrix[n-1][n]/matrix[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=matrix[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-matrix[i][j]*x[j]
        x[i]=x[i]/matrix[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,x[i]),end=" ")
```

## Output:

![image](https://github.com/rdxkeerthi/Gaussian/assets/147473120/de0b6aa7-785a-4c0d-98b0-6ec014cf46c8)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

