Given a range [m, n] where 0 <= m <= n <= 2147483647, return the bitwise AND of all numbers in this range, inclusive.

https://leetcode.com/problems/bitwise-and-of-numbers-range/

Python solution:
```
class Solution:
    def rangeBitwiseAnd(self, m: int, n: int) -> int:
        if n > m:
            return self.rangeBitwiseAnd(m>>1, n>>1) << 1
        else:
            return m
                 
```
