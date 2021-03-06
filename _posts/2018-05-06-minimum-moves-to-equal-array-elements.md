---
layout: post
title:  leetcode-453 minimum-moves-to-equal-array-elements
date:   2018-05-06 00:00:00
categories: LeetCode
tags: LeetCode-Easy
---

* content
{:toc}

This is another LeetCode Day

## Difficulty:

**Easy**

## Description：

Given a non-empty integer array of size n, find the minimum number of moves 
required to make all array elements equal, where a move is incrementing n - 1 elements by 1.

## Example：

```
Input:
[1,2,3]

Output:
3

Explanation:
Only three moves are needed (remember each move increments two elements):

[1,2,3]  =>  [2,3,3]  =>  [3,4,3]  =>  [4,4,4]
```

## Solution：

```
# 纯数学问题
[大神解释，摘录如下](https://leetcode.com/problems/minimum-moves-to-equal-array-elements/discuss/93817/It-is-a-math-question)
let’s define sum as the sum of all the numbers, before any moves; minNum as 
the min number int the list; n is the length of the list;
After, say m moves, we get all the numbers as x , and we will get the following equation
sum + m * (n - 1) = x * n
and actually,
x = minNum + m
and finally, we will get
sum - minNum * n = m
So, it is clear and easy now.

class Solution:
    def minMoves(self, nums):
        """
        :type nums: List[int]
        :rtype: int
        """
        return sum(nums) - min(nums) * len(nums)
```