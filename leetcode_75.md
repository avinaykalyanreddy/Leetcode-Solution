#  <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 75

Sort Colors. Click on the link to view the [Question](https://leetcode.com/problems/sort-colors/description/)


### Python  
```python

class Solution:
    def sortColors(self, nums: List[int]) -> None:
          low,mid,high = 0,0,len(nums)-1
          while mid <= high:

              if nums[mid] == 0:

                    nums[low],nums[mid] = nums[mid],nums[low]
                    low = low+1
                    mid = mid+1
              elif nums[mid] == 1:
                    mid = mid+1
              else:

                    nums[high],nums[mid] = nums[mid],nums[high]
                    high = high-1
          return nums
```

* low pointer to track the end of the 0s.  

* mid pointer to traverse through the list.  

* high pointer to track the start of the 2s.  

Traversal and Swapping:  


* If nums[mid] is 0, swap it with the element at low and increment both low and mid.  

* If nums[mid] is 1, just move the mid pointer.  

* If nums[mid] is 2, swap it with the element at high and decrement the high pointer.  
