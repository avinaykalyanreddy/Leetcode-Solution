# <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 1694

Reformat Phone Number. Click on the link to view the [question](https://leetcode.com/problems/reformat-phone-number/description/)

### Python
```python
def reformatNumber(number):

    store = []
    for i in number:
        if i != " " and i != "-":
               store.append(i)

    store = "".join(store)

    x = len(store); y = 0
    res = []

    while x:
          if x-3 >= 2  or x-3 == 0:   #5-3 = 2 0r 3-3 = 0
                  res.append(store[y:y+3])
                  y = y+3
                  x = x-3

          else:
               res.append(store[y:y+2])
               y = y+2
               x = x-2

    return "-".join(res)

reformatNumber("123 4-5678")
```
### output 🖥️
```
"123-456-78"
```

