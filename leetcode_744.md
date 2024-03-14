#  <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 744

**Find Smallest Letter Greater Than Target**. Click on the link to view the [question](https://leetcode.com/problems/find-smallest-letter-greater-than-target/)

### Python
```python
def nextGreatestLetter(letters,target):
      ans = '{'  # ASCII value of the character '{' is 123 and z is 122
      l = 0
      h = len(letters)-1

      while l<=h:

        mid = (l+h)//2
        if letters[mid]>target and letters[mid] < ans:
              ans = letters[mid]

        if target >= letters[mid]:
              l = mid+1
        else:

            h = mid-1
      return ans if ans != '{' else letters[0]
```
**time complexity -> O(log(n))**  

**space complexity -> O(1)**
### Output  🖥️
```
i/p-> letters = ["c","f","j"], target = "a"
o/p-> c
```

