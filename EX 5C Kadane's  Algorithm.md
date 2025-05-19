# EX 5C Kadane's Algorithm
## DATE: 22/04/25

## AIM:
To write a python program to find the maximum contiguous subarray.

## Algorithm
1. Initialize:

2. max_till_now = a[0]

3. max_ending = 0

4. Loop through each element of the array:

5. Add current element to max_ending

6. If max_ending < 0, reset it to 0

7. If max_ending > max_till_now, update max_till_now

8. Return max_till_now as the result.

## Program:

To implement the program to find the maximum contiguous subarray.

Developed by:Vidhyasri k

Register Number: 212222230170

```
def maxSubArraySum(a,size):
    
    
    max_till_now = a[0]
    max_ending = 0
    
    for i in range(0, size):
        max_ending = max_ending + a[i]
        if max_ending < 0:
            max_ending = 0
        
        
        elif (max_till_now < max_ending):
            max_till_now = max_ending
            
    return max_till_now
n=int(input())  
a =[] #[-2, -3, 4, -1, -2, 1, 5, -3]
for i in range(n):
    a.append(int(input()))
  
print("Maximum contiguous sum is", maxSubArraySum(a,n))
```

## Output:
![image](https://github.com/user-attachments/assets/f36b0a34-ec2a-44f2-b49a-1bd5d2d38320)


## Result:
Thus the program was executed successfully for finding the maximum contiguous sum of subarray..
