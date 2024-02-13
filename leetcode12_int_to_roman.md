

# <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 12

Click on the link to view the [question](https://leetcode.com/problems/integer-to-roman/description/)

### Code
```python
def int_to_roman(num):
  value = [1000,900,500,400,100,90,50,40,10,9,5,4,1]
  symbol  = ["M","CM","D","CD","C","XC","L","XL","X","IX","V","IV","I"]
  x = 0
  res = ""
  while(num>0):

    for i in range(num//value[x]):
      res = res+symbol[x]
      num = num-value[x]
    x = x+1

  return res

print(int_to_roman(3999))
```
### output
```
 MMMCMXCIX
```



