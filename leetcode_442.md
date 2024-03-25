#  <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 442  

**Find All Duplicates in an Array**. Click on the link to view the [question](https://leetcode.com/problems/find-all-duplicates-in-an-array/description/)   

## Python  

**Algorithm**  
This solution is for *integer array nums of length n where all the integers of nums are in the range [1, n]*  
1. Go through each number in the array one by one.
2. For each number, check if we've seen it before.  
    * for example if the example is 3 then check value at (3-1) index   
    * If the value at that index is negative, it means we've seen this number before (because we've already flipped it negative). So, we add it to our list of duplicates.  
    *  the value is positive, flip it negative to mark that we've seen this number.
3. Keep going through the entire array using this method.
4. Return the list of duplicates  found.




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
