## 1207. Unique Number of Occurrences

https://leetcode.com/problems/unique-number-of-occurrences

## Problem Description
```
Given an array of integers arr, return true if the number of occurrences of each value in the array is unique or false otherwise.
```

## Python Code

```py
class Solution(object):
    def uniqueOccurrences(self, arr):
        
        freq = {}
        
        for num in arr:
            if num not in freq:
                freq[num] = 1
            else:
                freq[num] += 1

        occurrences = []

        for num in freq:
            if freq[num] in occurrences:
                return False

            occurrences.append(freq[num])
        
        return True
```