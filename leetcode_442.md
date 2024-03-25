#  <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 442  

**Find All Duplicates in an Array**. Click on the link to view the [question](https://leetcode.com/problems/find-all-duplicates-in-an-array/description/)   

## Python  
```python
class Solution:
    def findDuplicates(self, nums: List[int]) -> List[int]:
        
        dup = []

        for i in nums:

            index = abs(i)-1

            if nums[index] < 0:

                dup.append(abs(i))

            else:

                nums[index] *= -1

        return dup
```
