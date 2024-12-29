
### Intersection of Two arrays with Duplicate Elements  

### Intersection of Two arrays with Duplicate Elements  

```
Input: a[] = [1, 2, 1, 3, 1], b[] = [3, 1, 3, 4, 1]
Output: [1, 3]
Explanation: 1 and 3 are the only common elements and we need to print only one occurrence of common elements.  

Input: a[] = [1, 1, 1], b[] = [1, 1, 1, 1, 1]
Output: [1]
Explanation: 1 is the only common element present in both the arrays.

Input: a[] = [1, 2, 3], b[] = [4, 5, 6]
Output: []
Explanation: No common element in both the arrays.
```

```python
class Solution:
    def intersectionWithDuplicates(self, a, b): 
        
        dic = {}
        
        for i in a:
            
            if i not in dic:
                
                dic[i] = 1
                
        
        res = []
        
        for i in b:
            
            if i in dic and dic[i] == 1:
                
                dic[i] = 0
                
                res.append(i)
                
                
        return sorted(res) 


```
