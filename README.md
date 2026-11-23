# LU Decomposition 

## AIM:
To write a program to find the LU Decomposition of a matrix.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. LU Decomposition (printing L and U)

Algorithm (4 steps):
Read the matrix A.
Perform LU decomposition of A to obtain P, L, and U.
Extract L (lower-triangular) and U (upper-triangular) matrices.
Display L and U.

2. Solving AX = B using LU Decomposition
   
Algorithm (4 steps):
Read matrices A and B and perform LU decomposition to get P, L, U.
Compute Pb by multiplying Pᵀ with B.
Solve the forward substitution Ly = Pb.
Solve the backward substitution Ux = y and print x.

## Program:
(i) To find the L and U matrix
'''
Program to find the L and U matrix.
Developed by:GOKUL N 
RegisterNumber:26009897 
'''
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np
from scipy.linalg import lu
a=np.array(eval(input()))
P,L,U=lu(a)
print(L)
print(U)

(ii) To find the LU Decomposition of a matrix
'''
Program to find the LU Decomposition of a matrix.
Developed by: GOKUL N
RegisterNumber: 26009897
'''
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np
from scipy.linalg import lu_factor,lu_solve
a=np.array(eval(input()))
b=np.array(eval(input()))
lu,pivot=lu_factor(a)
x=lu_solve((lu,pivot),b)
print(x)

## Output:
<img width="1267" height="830" alt="image" src="https://github.com/user-attachments/assets/4fb6f213-06c5-4af0-aa1d-d6854b6dc7fe" />
<img width="1295" height="755" alt="image" src="https://github.com/user-attachments/assets/35665a10-4d2f-4fff-94d9-f4c814a0d547" />



## Result:
Thus the program to find the LU Decomposition of a matrix is written and verified using python programming.

