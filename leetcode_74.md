#  <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 74  
**Search a 2D matrix**. Click on the link to view the [question](https://leetcode.com/problems/search-a-2d-matrix/description/)

### python
```python
def searchMatrix( matrix, target):

      for i in matrix:

          l = 0
          h = len(i)-1
          while l<= h:

              mid = (l+h)//2
              if i[mid] == target:
                        return True
              elif target > i[mid]:

                        l = mid+1
              else:
                  h = mid-1
      return False
```
**time complexity-> O(m*log(n))**  
**space complexity-> O(1)**

### output 🖥️
```
i/p-> matrix = [[1,3,5,7],[10,11,16,20],[23,30,34,60]], target = 3
o/p-> True
```
