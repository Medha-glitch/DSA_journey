# 🧹 Remove Element

**Leetcode Link:** [Remove Element](https://leetcode.com/problems/remove-element/)  
**Category:** Array  
**Difficulty:** Easy  

---

## 🔍 Problem Description

You are given an integer array `nums` and an integer `val`. Remove all occurrences of `val` in-place and return the number of elements remaining (not equal to `val`).

The first `k` elements of `nums` should hold the remaining elements.  
The order of elements **can change**.  
You don't need to consider the part of the array beyond `k`.

---

## 🧠 Approach & Intuition

We use a **two-pointer** approach:

- One pointer `i` to iterate over the array.
- One pointer `k` (or `res`) to keep track of the position to place the next valid element.

If `nums[i] != val`, we move it to `nums[k]` and increment `k`.

> The key idea: We overwrite the unwanted values (equal to `val`) with the next valid values.

This satisfies the "in-place" and "O(1) space" requirement.

---

## ✅ The Code

```python
class Solution:
    def removeElement(self, nums: List[int], val: int) -> int:
        k = 0  # Pointer for the position of the next valid element
        for i in range(len(nums)):
            if nums[i] != val:
                nums[k] = nums[i]
                k += 1
        return k
