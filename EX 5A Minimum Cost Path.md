# EX 5A Minimum Cost Path
## DATE: 15/04/25

## AIM:
To write a Python program using A Naive recursive implementation of Minimum Cost Path Problem.

## Algorithm
1. If m < 0 or n < 0: return ∞ (invalid path).

2. If m == 0 and n == 0: return cost[0][0] (start point).

3. Else:

4. Return cost[m][n] + min(
   
    minCost(m-1, n-1), (diagonal)
    
    minCost(m-1, n), (up)
    
    minCost(m, n-1) (left)
)

## Program:

A program to implement to find the Minimum Cost Path Problem using a  Naive recursive Approach.

Developed by: Vidhyasri k

Register Number: 212222230170
```
R = int(input())
C = int(input())
import sys
def minCost(cost, m, n):
  
    if (n < 0 or m < 0):
        return sys.maxsize
    elif (m == 0 and n == 0):
        return cost[m][n]
    else:
        return cost[m][n] + min( minCost(cost, m-1, n-1),
                                minCost(cost, m-1, n),
                                minCost(cost, m, n-1) )
def min(x, y, z):
    if (x < y):
        return x if (x < z) else z
    else:
        return y if (y < z) else z
cost= [ [1, 2, 3],
        [4, 8, 2],
        [1, 5, 3] ]
print(minCost(cost, R-1, C-1))
```


## Output:
![image](https://github.com/user-attachments/assets/c98a0336-b28e-4a0c-8aa6-993b886f8f8f)


## Result:
Thus the above program was executed successfully for finding the minimum cost.
