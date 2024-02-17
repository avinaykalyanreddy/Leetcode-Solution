# <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 338

Counting Bits. Click on the link to view the [Question](https://leetcode.com/problems/counting-bits/description/?envType=study-plan-v2&envId=leetcode-75)

### Python

```python

def countBits(n):

    res = []

    for i in range(0,n+1):

          if i == 0:
                res.append(0)

          else:
              x = 0

              while i>1:
                    if i % 2 == 1:
                        x = x+1
                    i  = i//2
              x = x+1
              res.append(x)

    return res
```
### Output
```
[0,1,1,2,1,2]
```

### Complexity

Time complexity -> **N(logN)**  
Space complexity -> **N**
