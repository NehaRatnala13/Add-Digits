# 258. Add Digits

**Difficulty:** Easy | **Topics:** Math, Simulation, Number Theory  
**Problem Link:** [LeetCode 258 - Add Digits](https://leetcode.com/problems/add-digits/)

---

## 📝 Problem Description

Repeatedly add all digits of an integer `num` until the result has only one digit, and return it.

* **Example 1:** `num = 38` \(\rightarrow\) `3 + 8 = 11` \(\rightarrow\) `1 + 1 = 2` (Output: `2`)
* **Example 2:** `num = 0` (Output: `0`)
* **Constraints:** \(0 \le \text{num} \le 2^{31} - 1\)
* **Follow-up:** Can you solve it in \(O(1)\) time without any loop or recursion?

---

## 💡 Intuition & Approaches

* **Approach 1: Iterative Simulation** — Repeatedly sum digits via modulo and division until a single digit remains (\(O(\log n)\) time, \(O(1)\) space).
* **Approach 2: Mathematical (Digital Root)** — Leveraging the repeating base-9 digital root pattern \([1 + ((\text{num} - 1) \bmod 9)]\) for \(n > 0\), or \(0\) if \(\text{num} == 0\) (\(O(1)\) time, \(O(1)\) space).

---

## 💻 Solutions

### Python
```python
class Solution:
    def addDigits(self, num: int) -> int:
        return 0 if num == 0 else 1 + (num - 1) % 9
```

