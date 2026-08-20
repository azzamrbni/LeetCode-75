## 1004. Max Consecutive Ones III

https://leetcode.com/problems/max-consecutive-ones-iii

## Problem Description
```
Given a binary array nums and an integer k, return the maximum number of consecutive 1's in the array if you can flip at most k 0's.
```

## Python Code

```py
class Solution(object):
    def longestOnes(self, nums, k):
        
        left = 0
        countnow = 0
        countmax = 0
        countzero = 0

        for right in range(len(nums)):
            if nums[right] == 0:
                countzero += 1

            while countzero > k:
                if nums[left] == 0:
                    countzero -= 1
                left += 1

            countnow = right - left + 1
            if countnow > countmax:
                countmax = countnow

        return countmax
```