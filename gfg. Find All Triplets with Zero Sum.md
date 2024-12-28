

### Given an array arr[], find all possible triplets i, j, k in the arr[] whose sum of elements is equals to zero. 
Returned triplet should also be internally sorted i.e. i<j<k.


```
Input: arr[] = [0, -1, 2, -3, 1]
Output: [[0, 1, 4], [2, 3, 4]]
Explanation: Triplets with sum 0 are:
arr[0] + arr[1] + arr[4] = 0 + (-1) + 1 = 0
arr[2] + arr[3] + arr[4] = 2 + (-3) + 1 = 0
```

```python
class Solution:
    def findTriplets(self, arr):
        
        dic = {}  # store a unique pairs of indices
        
        for i in range(len(arr)):
            
            for j in range(i+1,len(arr)):   # why (0,1) and (1,0) here (1,0) is redundancy  so we are not iterating from 0th index
                
                s = arr[i]+arr[j]
                
                if s not in dic:
                    
                    dic[s] = []
                    
                dic[s].append((i,j))
                
        triplets = set()
        
        for i in range(len(arr)):
            
            r = -arr[i]
            
            if r in dic:
                
                for j,k in dic[r]:
                    
                    if j != i and k != i:
                        
                        ar = sorted([i,j,k])
                        
                        triplets.add(tuple(ar))
                        
        return [list(i) for i in triplets]
                
```
