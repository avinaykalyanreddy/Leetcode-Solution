#  <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 1

Two sum. Click on the link to view the [Question](https://leetcode.com/problems/two-sum/description/)

### Python



```python

class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
      
      dic = {}
      
      for i in range(len(nums)):
          
          dic[nums[i]] = i
          
          
      for  k in range(len(nums)):
          
          x = target - nums[k]
          
          if x in dic and k != dic[x]:
              
              return [k,dic[x]]

```

### Output  🖥️
```
[1,2]
```
