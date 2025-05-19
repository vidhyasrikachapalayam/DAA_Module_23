# EX 5B Coin Change Problem
## DATE: 19/04/25

## AIM:
To compute the fewest number of coins that we need to make up the amount given.

## Algorithm
1. Input: List of coin denominations coins and total amount.

2. Initialize dp[0] = 0 and all other dp[i] = ∞ (1D array of size amount + 1).

3. For each coin in coins:

   For i = coin to amount:

   Update dp[i] = min(dp[i], dp[i - coin] + 1)

4. If dp[amount] == ∞, return -1 (not possible); else return dp[amount].


## Program:

Create a python function to compute the fewest number of coins that we need to make up the amount given.

Developed by:Vidhyasri k 

Register Number: 212222230170

```
class Solution(object):
   def coinChange(self, coins, amount):
 
       dp = [float('inf')] * (amount + 1)
       dp[0]=0
       for coin in coins:
           for i in range(coin, amount + 1):
               dp[i] = min(dp[i], dp[i - coin] + 1)
       return dp[amount] if dp[amount]!=float('inf') else -1
      
ob1 = Solution()
n=int(input())
s=[]
amt=int(input())
for i in range(n):
    s.append(int(input()))


print(ob1.coinChange(s,amt))
```

## Output:
![image](https://github.com/user-attachments/assets/705d2654-607f-46d1-9f20-923316167037)


## Result:
Thus the program was executed successfully for finding the minimum number of coins required to make amount.
