#  <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 881
**Boats to Save People**. Click on the link to view the  [Question](https://leetcode.com/problems/boats-to-save-people/description/?envType=daily-question&envId=2024-05-04)

Python
```python
class Solution:
    def numRescueBoats(self, p: List[int], limit: int) -> int:
        p.sort()
        x=0
        l, r=0, len(p)-1
        while l<=r:
            x+=1
            if p[l]+p[r]<=limit:
                l+=1
            r-=1
        return x
```

