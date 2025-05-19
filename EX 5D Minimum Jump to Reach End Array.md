# EX 5D Minimum Jump to Reach End Array
## DATE: 26/04/25

## AIM:
To write a python program for finding the minimum number of jumps needed to reach end of the array using Dynamic Programming.


## Algorithm
1. If n == 0 or arr[0] == 0, return ∞ (not reachable).

2. Initialize jumps[0] = 0; rest as ∞.

3. For each index i from 1 to n-1:

4. For each index j from 0 to i-1:

5. If i <= j + arr[j] and jumps[j] is not ∞:

6. Set jumps[i] = jumps[j] + 1

7. Break

8. Return jumps[n-1] as the minimum number of jumps.
   
## Program:

To implement the program to finding the minimum number of jumps needed to reach end of the array.

Developed by: Vidhyasri k

Register Number: 212222230170

```
def minJumps(arr, n):

    jumps = [0 for i in range(n)]
 
    if (n == 0) or (arr[0] == 0):
        return float('inf')
 
    jumps[0] = 0
    for i in range(1, n):
        jumps[i] = float('inf')
        for j in range(i):
            if (i <= j + arr[j]) and (jumps[j] != float('inf')):
                jumps[i] = min(jumps[i], jumps[j] + 1)
                break
    return jumps[n-1]
arr = []
n = int(input()) #len(arr)
for i in range(n):
    arr.append(int(input()))
print('Minimum number of jumps to reach','end is', minJumps(arr,n))
 
```
## Output:
![image](https://github.com/user-attachments/assets/c1926308-92a8-4962-b061-0aaf7629d7f8)


## Result:
Thus the program was executed successfully for finding the minimum number of jumps to reach end.
