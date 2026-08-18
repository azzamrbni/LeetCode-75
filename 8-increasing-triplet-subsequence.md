## 334. Increasing Triplet Subsequence

https://leetcode.com/problems/increasing-triplet-subsequence

## Problem Description
```
Given an integer array nums, return true if there exists a triple of indices (i, j, k) such that i < j < k and nums[i] < nums[j] < nums[k]. If no such indices exists, return false.
```

## Python Code

```py
class Solution(object):
    def increasingTriplet(self, nums):
        x1 = float('inf')
        x2 = float('inf')

        for n in nums:
            if n <= x1:
                x1 = n
            elif n <= x2:
                x2 = n
            else:
                return True
        return False
```