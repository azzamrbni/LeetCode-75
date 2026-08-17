## 1431. Kids With the Greatest Number of Candies

https://leetcode.com/problems/kids-with-the-greatest-number-of-candies

## Problem Description
```
There are n kids with candies. You are given an integer array candies, where each candies[i] represents the number of candies the ith kid has, and an integer extraCandies, denoting the number of extra candies that you have.

Return a boolean array result of length n, where result[i] is true if, after giving the ith kid all the extraCandies, they will have the greatest number of candies among all the kids, or false otherwise.

Note that multiple kids can have the greatest number of candies.
```

## Python Code

```py
class Solution(object):
    def kidsWithCandies(self, candies, extraCandies):
        
        maxCandies = max(candies)

        result = []
        for i in range(len(candies)):
            result.append(candies[i] + extraCandies >= maxCandies)

        return result
```