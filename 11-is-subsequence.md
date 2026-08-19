## 392. Is Subsequence

https://leetcode.com/problems/is-subsequence

## Problem Description
```
Given two strings s and t, return true if s is a subsequence of t, or false otherwise.

A subsequence of a string is a new string that is formed from the original string by deleting some (can be none) of the characters without disturbing the relative positions of the remaining characters. (i.e., "ace" is a subsequence of "abcde" while "aec" is not).
```

## Python Code

```py
class Solution(object):
    def isSubsequence(self, s, t):
        
        scount = len(s)
        j = 0
        
        if s != "":
            for i in range(len(t)):
                if scount != 0 and s[j] == t[i]:
                    j += 1
                    scount -= 1

        return scount == 0
        
```