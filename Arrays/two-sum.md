# 🧮 Two Sum

**Problem Link**: [Two Sum – LeetCode](https://leetcode.com/problems/two-sum/)  
**Category**: Arrays  
**Difficulty**: Easy

---

## 🧠 Problem Statement

Given an array of integers `nums` and an integer `target`, return indices of the two numbers such that they add up to `target`.

---

## 🧩 Approach

### Brute Force:
- Try every pair using two nested loops.
- Time: O(n²)

### Optimal (Using Hash Map):
- Use a dictionary to store `target - nums[i]` while traversing.
- Time: O(n), Space: O(n)

---

## ✅ Code (Python)

```python
def twoSum(nums, target):
    hash_map = {}
    for i, num in enumerate(nums):
        if target - num in hash_map:
            return [hash_map[target - num], i]
        hash_map[num] = i
