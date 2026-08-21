## 2215. Find the Difference of Two Arrays

https://leetcode.com/problems/find-the-difference-of-two-arrays

## Problem Description
```
Given two 0-indexed integer arrays nums1 and nums2, return a list answer of size 2 where:

answer[0] is a list of all distinct integers in nums1 which are not present in nums2.
answer[1] is a list of all distinct integers in nums2 which are not present in nums1.
Note that the integers in the lists may be returned in any order.
```

## Python Code

```py
class Solution(object):
    def findDifference(self, nums1, nums2):
        
        list = []
        list1 = []
        list2 = []

        for i in range(len(nums1)):
            if nums1[i] not in nums2 and nums1[i] not in list1:
                list1.append(nums1[i])

        for i in range(len(nums2)):
            if nums2[i] not in nums1 and nums2[i] not in list2: 
                list2.append(nums2[i])
        
        list.append(list1)
        list.append(list2)

        return list
```