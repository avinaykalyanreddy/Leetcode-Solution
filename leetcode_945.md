#  <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 945

Minimum Increment to Make Array Unique. Click on the link to view the [Question](https://leetcode.com/problems/minimum-increment-to-make-array-unique/description/)  

## Python

```python
class Solution:
    def minIncrementForUnique(self, nums: List[int]) -> int:

            nums.sort()
            moves = 0
            pre = nums[0]

            for i in range(1,len(nums)):

                  if nums[i] <= pre:
                          pre = pre+1

                          moves += pre-nums[i]
                  else:

                      pre = nums[i]
            return moves         
```

## Explaination

1. Sort the array.
2. Initialize the variables:
     * 'moves' to keep track  of the total number of moves required.
     * 'pre' to keep the track of the previous element to ensure uniqueness.
3. iterate through the array.
     * if the current element is less than or equal to the pre then increment pre, and calculate difference between pre and current element and add to the 'moves' variable.
     * if current element is greater than pre, set pre to nums[i].
4. Return the 'moves'

## Complexity

space --> O(1)  

time --> O(nlog(n))
   
   
    
