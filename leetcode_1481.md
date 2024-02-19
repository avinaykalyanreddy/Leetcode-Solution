# <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 1481

Click on the link to view the [question](https://leetcode.com/problems/least-number-of-unique-integers-after-k-removals/description/)

### Python
```python
def findLeastNumOfUniqueInts(arr,k):

      dic = {}

      for i in arr:
            if i not in dic:
                  dic[i] = 1

            else:
                  dic[i] += 1

      values = sorted(dic.values())

      x = 0  # to track the index of values
      res = 0

      for i in values:
            if k>= i:
                  k = k-i
                  values[x] = 0

            else:
                  values[x] = k-i
                  k = 0

            if values[x] != 0:
                  res = res+1

            x = x+1
      return res
findLeastNumOfUniqueInts(arr = [4,3,1,1,3,3,2], k = 3)
```
### output 🖥️
```
2
```


