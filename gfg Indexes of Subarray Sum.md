# Given an array arr[] containing only non-negative integers, your task is to find a continuous subarray (a contiguous sequence of elements) whose sum equals a specified value target. You need to return the 1-based indices of the leftmost and rightmost elements of this subarray. You need to find the first subarray whose sum is equal to the target.

Note: If no such array is possible then, return [-1].

```text
Input: arr[] = [1, 2, 3, 7, 5], target = 12
Output: [2, 4]
Explanation: The sum of elements from 2nd to 4th position is 12.

Input: arr[] = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10], target = 15
Output: [1, 5]
Explanation: The sum of elements from 1st to 5th position is 15.

Input: arr[] = [5, 3, 4], target = 2
Output: [-1]
Explanation: There is no subarray with sum 2.
```
```python
class Solution:
    def subarraySum(self, arr, target):  
    
            s = 0
            index = 0

            for i in range(len(arr)):

                s += arr[i] 
                
                while s > target:
                    
                    s -= arr[index]
                    
                    index += 1
                    
                if s == target:
                    
                    return [index+1,i+1]
                
            return [-1]
```
# Explaination

* initially add current index value with the variable s .
* And check if s > than target if true then minus s with arr[index] index is the subarray 0th index.
* check with s is equal to target then return [index+1,i+1].
* else return [-1]

Time and Space compexity is O(n) and O(1)
