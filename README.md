# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. First,we want to import numpy,then import sys,assume a variable.
2. For gaussian elimination method, we want to make 2nd and 3rd column zero.
3. For that we want to make a range accorting to our program output.
4. Then print the program with correct form then the output will display.

## Program:
```
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: YASHVANDAN K
RegisterNumber: 212225100060
'''
import numpy as np
n=int(input())
a=[]
for i in range(n):
    row=[]
    for j in range(n+1):
        row.append(float(input()))
    a.append(row)
a=np.array(a,dtype=float)
for i in range(n):
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x=np.zeros(n)
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
        x[i]=x[i]/a[i][i]
for i in range(n):
    print(f"X{i} = {x[i]:.2f}",end=" ")
```

## Output:
![alt text](<Screenshot 2026-02-27 221736.png>)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

