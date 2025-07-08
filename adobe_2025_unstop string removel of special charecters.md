

### Given string it consist of special symols like $,#,* remove sepcial symbols and right most nearest aplhabet

### note string may contain space

```python
s = "th w$g## bjhdwdvdg*gh$vvdd#bdud hc"

n = len(s)
chars = ["$", "#", "*"]
i = len(s) - 1

lst = [False] * n

while i >= 0:
    if s[i] in chars:
        lst[i] = True
        j = i + 1
        while j < n:
            if not lst[j] and s[j].isalpha():
                lst[j] = True
                break
            j += 1
    i -= 1

result = "".join([s[i] for i in range(n) if not lst[i]])
print(result)



```
