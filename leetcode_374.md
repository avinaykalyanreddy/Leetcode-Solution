#  <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 374
**Guess Number High or Low**. Click on the link to view the [question](https://leetcode.com/problems/guess-number-higher-or-lower/)  

### Python
```python

pick = int(input("Enter number-> ")
def guess(num):

    if num > pick:
        return -1
    
    elif num < pick:
        return 1
    
    else:
        return 0
def guessNumber( n) ->:

    l = 1
    r = n

    while l<= r:

        mid = (l+r)//2
        g = guess(mid)

        if g == 0:
            return (mid)
            

        elif g == -1:

            r = mid-1

        else:
            l = mid+1
```
**time complexity -> O(log(n))**  
**space complecity -> O(1)**  
### output 🖥️
```
i/p-> n = 10, pick = 6
o/p-> 6
```
