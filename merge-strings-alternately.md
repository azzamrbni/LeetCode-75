## 1768. Merge Strings Alternately

https://leetcode.com/problems/merge-strings-alternately

## Description
```
You are given two strings word1 and word2. Merge the strings by adding letters in alternating order, starting with word1. If a string is longer than the other, append the additional letters onto the end of the merged string.

Return the merged string.
```

## Python Code

```py
class Solution(object):
    def mergeAlternately(self, word1, word2):
        result = ""

        for i in range(max(len(word1), len(word2))):
            
            if i < len(word1):
                result += word1[i]

            if i < len(word2):
                result += word2[i]

        return result
```