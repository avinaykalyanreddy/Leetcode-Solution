
**Iterate from last and find the first occurance of odd from right to left and return string 0 to odd numbered index**

```python
s = '6163286'

for i in range(len(s)-1,-1,-1):

    if int(s[i]) % 2 != 0:

        print(s[0:i+1])
        break
```
