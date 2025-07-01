## 🧩 Pattern: Frequency Map / Character Count

**Concept**: Compare character frequenices using an array/hash map.

**Template**: 
- Count occurrences of each car in 's' and 't'.
- Compare both.
- Return 'True' if counts match, else 'False'.

**Problem**: - [Valid Anagram](https://leetcode.com/problems/valid-anagram/)

**Time Complexity**: O(n)

**Space Complexiy**: O(1)

## Example
``` python
def isAnagram(s, t):
    if len(s) != len(t):
        return False

    count = [0] * 26  # Or use collections.Counter for general characters

    for i in range(len(s)):
        count[ord(s[i]) - ord('a')] += 1
        count[ord(t[i]) - ord('a')] -= 1

    for val in count:
        if val != 0:
            return False
    return True
```
