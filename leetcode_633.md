#  <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 633

Sum of Square Numbers. Click on the link to view the [Question](https://leetcode.com/problems/sum-of-square-numbers/description/)  

## Python   
```python
class Solution:
    def judgeSquareSum(self, c: int) -> bool:

              low = 0
              high = int(c**0.5)+1

              while low <= high:
                    sum = low*low + high*high

                    if sum == c:
                          return True
                    elif sum > c:
                          high = high -1
                    else:
                        low = low+1
              return False

```

        
