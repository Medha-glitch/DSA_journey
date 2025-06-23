# 🧩 LeetCode 88 — Merge Sorted Array

## 🔍 Problem Statement
You are given two sorted integer arrays `nums1` and `nums2`, and two integers `m` and `n` representing the number of elements in each.

- `nums1` has a size of `m + n`, with the first `m` elements valid and the rest as `0`s.
- `nums2` has `n` elements.
- Merge `nums2` into `nums1` in-place, so that `nums1` becomes a single sorted array.

---

## ✅ Approach: Two Pointers (From the Back)

### Why merge from the back?
If we start from the front, we risk **overwriting** the valid data in `nums1`.  
By starting from the end, we can safely place the **largest elements** first using three pointers:

- `i`: points to last valid value in `nums1`
- `j`: points to last value in `nums2`
- `k`: points to last available index in `nums1`

---

## 🔁 Step-by-Step Logic

1. Compare `nums1[i]` and `nums2[j]`
2. Place the **larger value** at `nums1[k]`
3. Move the appropriate pointer (`i` or `j`) and decrement `k`
4. If any elements are left in `nums2`, copy them

---

## 💡 Example

```python
nums1 = [1,2,3,0,0,0]
m = 3
nums2 = [2,5,6]
n = 3
