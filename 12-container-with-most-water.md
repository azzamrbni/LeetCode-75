## 11. Container With Most Water

https://leetcode.com/problems/container-with-most-water

## Problem Description
```
You are given an integer array height of length n. There are n vertical lines drawn such that the two endpoints of the ith line are (i, 0) and (i, height[i]).

Find two lines that together with the x-axis form a container, such that the container contains the most water.

Return the maximum amount of water a container can store.

Notice that you may not slant the container.
```

## Python Code

```py
class Solution(object):
    def maxArea(self, height):
        kiri = 0
        kanan = len(height) - 1
        luasmax = 0

        while kiri < kanan:
            lebar = kanan - kiri
            tinggi = min(height[kanan], height[kiri])
            luasnow = lebar * tinggi

            if luasnow > luasmax:
                luasmax = luasnow

            if height[kiri] < height[kanan]:
                kiri += 1
            else:
                kanan -= 1

        return luasmax
```