#  <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 2485

Find the pivot integer. Click on the link to view the [question](https://leetcode.com/problems/find-the-pivot-integer/description/)

### Python
```python

def pivotInteger(n):      #pivot -> sum(1 to x) == sum(x to n)
    half = n//2

    while(half<=n):

        a = (half*(half+1))//2       # sum(1 to half)
        b = (n*(n+1)//2) - a + half   # sum(half to n)
        if a-b == 0:
              return half
        else:
            half = half+1

    else:
        return -1
```
### output 🖥️
```
i/p-> n = 8
o/p -> 6
```
