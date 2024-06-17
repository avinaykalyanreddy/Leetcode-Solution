#  <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 6

Zigzag Conversion. Click on the link to view the [Question](https://leetcode.com/problems/zigzag-conversion/description/)

## Python

### My solution
```python
class Solution:
    def convert(self, s: str, numRows: int) -> str:

        if numRows == 1 or numRows >= len(s):

            return s
        result = [[] for i in range(numRows)]

        count = 0
        signal = 0

        for i in s:
            
            result[count].append(i)

            if count == numRows-1:
                signal = 1
            
            if signal == 1:
                count = count-1

            if count == -1:
                
                signal = 0
                count = 0


            if signal == 0:
                
                count = count+1

        res = []

        for i in result:
            
            for k in i:
                
                res.append(k)

        return("".join(res))
```
### Chat GPT solution

```python
class Solution:
    def convert(self, s: str, numRows: int) -> str:

              if numRows == 1 or numRows >= len(s):
                    return s

              result = [""]*numRows
              current_row = 0
              direction = -1 # -1 means going up, +1 means going down in matrix
              for i in s:

                  result[current_row] += i
                  if current_row == 0 or current_row == numRows-1:

                          direction *= -1
                  current_row += direction
              return "".join(result)
```



            

