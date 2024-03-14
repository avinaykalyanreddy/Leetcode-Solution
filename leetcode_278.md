#  <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 278
**First bad version**. Click on the link to view the [question](https://leetcode.com/problems/first-bad-version)

### python
```python
def isBadVersion(version):

    if version >= bad:
        return True
    
    return False

def firstBadVersion(n):    
        l = 0
        r = n
        while(l<r):

            mid = (l+r)//2

            if isBadVersion(mid):

                r = mid

            else:
                l = mid+1

        return (r)
```
**time complexity -> O(log(n))**  
**space complexity -> O(1)**  
### output 🖥️
```
i/p-> n = 5, bad = 4
o/p-> 4
```
