# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
### Step 1:
First,we want to import numpy,then import sys,assume a variable.
### Step 2:
For gaussian elimination method, we want to make 2nd and 3rd column zero.
### Step 3:
For that we want to make a range accorting to our program output.
### Step 4:
Then print the program with correct form then the output will display.
### Step 5:
End the program.

## Program:
```

Program to find the solution of a matrix using Gaussian Elimination.
Developed by: VESLIN ANISH
RegisterNumber: 212223240175
import numpy as np
import sys 
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]= float(input())
for i in range(n):
    if a[i][i] ==0.0: 
        sys.exit("Divide by zero detected!")
    for j in range(i+1,n):
        ratio = a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k] = a[j][k] - ratio * a[i][k]
x[n-1] = a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i] = a[i][n]
    for j in range(i+1,n):
        x[i] = x[i] - a[i][j]*x[j]
    x[i] = x[i]/a[i][i]
for i in range(n):
    print("X%d = %0.2f " %(i,x[i]) , end = "")

```

## Output:
![WhatsApp Image 2024-04-16 at 15 55 06_dc1fe301](https://github.com/veslin23000303/Gaussian/assets/151148539/461dcdb1-2d25-46fa-b61e-f4cda8258136)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

