## Reverse Words in a String

https://leetcode.com/problems/reverse-words-in-a-string

## Problem Description
```
Given an input string s, reverse the order of the words.

A word is defined as a sequence of non-space characters. The words in s will be separated by at least one space.

Return a string of the words in reverse order concatenated by a single space.

Note that s may contain leading or trailing spaces or multiple spaces between two words. The returned string should only have a single space separating the words. Do not include any extra spaces.
```

## Python Code (Optimized)

```py
class Solution(object):
    def reverseWords(self, s):
        return " ".join(s.split()[::-1])
```

## Python Code

```py
class Solution(object):
    def reverseWords(self, s):
        s = list(s)
        box = []

        for i in range(len(s)):
            bucket = []
            if s[i] != " ":
                while i < len(s) and s[i] != " ":
                    bucket.append(s[i])
                    i += 1
                word = "".join(bucket)
                box.append(word)

        left = 0
        right = len(box) - 1
        while left < right:
            box[left], box[right] = box[right], box[left]
            left += 1
            right -= 1

        return " ".join(box)
```