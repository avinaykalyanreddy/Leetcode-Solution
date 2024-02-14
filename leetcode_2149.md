# <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 2149


###  Rearrange Array Elements by Sign. Click on the link to view the  [question](https://leetcode.com/problems/rearrange-array-elements-by-sign/?envType=daily-question&envId=2024-02-14)

## Python

```python
class Solution(object):
    def rearrangeArray(self, nums):

        res = [-1]*len(nums)

        p = 0
        n = 1

        for i in nums:

            if i>0 :
                res[p] = i
                p = p+2

            else:
                res[n] = i
                n = n+2
        
        return res

```
## output 🖥️
```
[3,-2,1,-5,2,-4]
```
