## 1493. Longest Subarray of 1's After Deleting One Element

https://leetcode.com/problems/longest-subarray-of-1s-after-deleting-one-element

## Problem Description
```
Given a binary array nums, you should delete one element from it.

Return the size of the longest non-empty subarray containing only 1's in the resulting array. Return 0 if there is no such subarray.
```

## Python Code

```py
class Solution(object):
    def longestSubarray(self, nums):
        left = 0
        countnow = 0
        countmax = 0
        countzero = 0

        for right in range(len(nums)):
            if nums[right] == 0:
                countzero += 1

            while countzero > 1:
                if nums[left] == 0:
                    countzero -= 1
                left += 1

            countnow = right - left
            if countnow > countmax:
                countmax = countnow

        return countmax
```