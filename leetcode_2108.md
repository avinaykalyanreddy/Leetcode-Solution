# <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 2108

### Find the palindromic string in the array. click on the link to view the [question](https://leetcode.com/problems/find-first-palindromic-string-in-the-array/description/?envType=daily-question&envId=2024-02-13)
## Python
```python
def firstPalindrome(words):

   for i in words:
        j = 0
        k = len(i)-1
        while(j<=k):
            
            if (i[j] != i[k]):
                      j = 0
                      break
  
            j = j+1
            k = k-1
  
        if (j != 0):
            return i
   return ""
```
## output 🖥️

 #### **firstPalindrome(["abc","car","ada","racecar","cool"])  ---> ada**

## Explaination

let understand what is palindrome, if we read a word from left to right and right to left should be equal then we can say that it is a palindrome. 

#### example


<img src="https://shorturl.at/fKPY9">

1. Iterate each elements in a lis(words)
2. i represent the each word from the list(words)
3. Declare a two variables for tacking the index, initially j = 0(first index) and k = len(i)-1 (last index)
4. Use while loop, the condition should be (j <= k because left index always smaller than right index of string ) and check if i[j] is equal or not equal to i[k]
5. Then check j != 0 because if j = 0 then the current word (i) not a palindrome. j != 0 then it is a palindrome
6. Final line if any of above condition is not satisfying then return empty String



