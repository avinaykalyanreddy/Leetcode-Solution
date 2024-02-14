# <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 13

### Roman to Integer. click on the link to view the [question](https://leetcode.com/problems/roman-to-integer/description/)

## Python
```python

def romanToInt(self, s):
    dic = {"M": 1000, "CM": 900, "D": 500, "CD": 400, "C": 100, "XC": 90, "L": 50, "XL": 40, "X": 10, "IX": 9, "V": 5, "IV": 4, "I": 1}
    i = 0
    res = 0

    while(i < len(s)):

        if (i < len(s)-1 and s[i]+s[i+1] in dic):

            res = res+dic[s[i]+s[i+1]]
            i = i+2

        else:
            res = res+dic[s[i]]
            i = i+1

    return res
obj.romanToInt("MMMCMXCIX")

```

## output 🖥️
```
3999
```
