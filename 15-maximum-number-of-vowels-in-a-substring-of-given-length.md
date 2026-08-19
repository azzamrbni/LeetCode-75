## 1456. Maximum Number of Vowels in a Substring of Given Length

https://leetcode.com/problems/maximum-number-of-vowels-in-a-substring-of-given-length

## Problem Description
```
Given a string s and an integer k, return the maximum number of vowel letters in any substring of s with length k.

Vowel letters in English are 'a', 'e', 'i', 'o', and 'u'.
```

## Python Code

```py
class Solution(object):
    def maxVowels(self, s, k):
        
        vowels = ['a', 'i', 'u', 'e', 'o']
        countnow = 0

        for i in range(k):
            if s[i] in vowels:
                countnow += 1
            
        countmax = countnow

        for i in range(k, len(s)):
            if s[i] in vowels:
                countnow += 1

            if s[i - k] in vowels:
                countnow -= 1

            if countnow > countmax:
                countmax = countnow

        return countmax
```