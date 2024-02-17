#  <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 1

Two sum. Click on the link to view the [Question](https://leetcode.com/problems/two-sum/description/)

### Python

```python

def twoSum(nums,target):

    dic = {}
    for i in range(len(nums)):
        if nums[i] not in dic:
            dic[nums[i]] = [i]
        else:
              dic[nums[i]].append(i)

    for i in nums:
        if target-i in dic:

              if i == target-i and len(dic[i])  != 1:
                     return [dic[i].pop(),dic[i].pop()]
              elif i != target-i:
                     return [dic[i].pop(),dic[target-i].pop()]

twoSum(nums = [3,2,4], target = 6)

```
### Output  🖥️
```
[1,2]
```
