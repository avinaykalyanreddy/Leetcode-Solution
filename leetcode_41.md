#  <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 41  

First missing positive integer. Click on the link to view the [question](https://leetcode.com/problems/first-missing-positive/description/)  

## Python  

### Algorithm  


1. Replace negative integers with 0 because we need to find First missing positive integer.

2. for each element in nums do the following operations.    
    *  index = abs(nums[i])-1   
    * now check the index in range 0 to less than len(nums)     
    * if nums[index] > 0 then nums[index] *= -1 because the value index+1 in nums array

    * if the current value is 0 then nums[index] = -len(nums)

3. now iterate the modified list. if the value encounter with positive number  then return current index + 1 , it is the smallest missing number.
4. If no positive value is found, print len(nums) + 1, indicating that all positive integers up to len(nums) are present in the list.

**Solution 1**
```python
class Solution:
    def firstMissingPositive(self, nums: List[int]) -> int:

        for i in range(len(nums)):

            if nums[i] < 0:
                nums[i] = 0

        for  i in range(len(nums)):

            index = abs(nums[i]) - 1

            if 0<= index < len(nums):

                if nums[index] > 0:

                    nums[index] *= -1

                elif nums[index] == 0:

                    nums[index] = -len(nums)

        
        for i in range(len(nums)):

            if nums[i] >= 0:

                return i+1

        
        return len(nums)+1
```
**Time complexity O(n)**  
**Space complexity O(1)**  

**Solution 2**
```python
class Solution:
    def firstMissingPositive(self, nums: List[int]) -> int:
        nums.sort()
        x = 1
        for i in nums:
              if x == i:
                  x = x+1

        return x

```
**Time complexity O(nlogn)**  
**Space complexity O(1)**  

**Solution 3** 

```python
class Solution:
    def firstMissingPositive(self, nums: List[int]) -> int:

          dic = {}
          for i in nums:
               dic[i] = 0

          for i in range(1,len(nums)+1):

                      if i not in dic:
                          return i
          return i+1
```
**Time complexity O(n)**  
**Space complexity O(n)**  


                  




