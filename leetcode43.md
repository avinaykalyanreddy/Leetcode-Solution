# <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 43

###  Multiply Strings. click on the link to view the [question](https://leetcode.com/problems/multiply-strings/description/)
## Python

```python
def multiply(num):

    res = 0

    for i in num:

        res = res*10 + ord(i)-48

    return res

x = multiply("123")
y = multiply("456")

print(str(x*y))
```

## output 🖥️

#### **"56088"**
