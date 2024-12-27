
### Given an array arr[] and an integer target. You have to find numbers of pairs in array arr[] which sums up to given target.

```
Input: arr[] = [1, 5, 7, -1, 5], target = 6 
Output: 3
Explanation: Pairs with sum 6 are (1, 5), (7, -1) and (1, 5). 
```

```
Input: arr[] = [1, 1, 1, 1], target = 2 
Output: 6
Explanation: Pairs with sum 2 are (1, 1), (1, 1), (1, 1), (1, 1), (1, 1).
```

```
Input: arr[] = [10, 12, 10, 15, -1], target = 125
Output: 0
```   

---> current index in second loop should be less than the index of arr in dic  

```python
class Solution:
    
    def countPairs(self,arr, target):
        
        
        dic = {}
        
        for i in range(len(arr)):
            
            
            if arr[i] not in dic:
                
                dic[arr[i]] = [i]
                
            else:
                
                dic[arr[i]].append(i)
                
                
        res = 0
        
        for i in range(len(arr)):
            
            x = target - arr[i]
            
            if x in dic:
                
                for j in dic[x]:
                    
                    if i < j:
                        
                        res = res+1
                        
        return res


```

Time complexity : O(n)  
Space complexity : O(n)

```python
arr = [1, 1, 1, 1]; target = 2

res = 0
dic = {}

for i in arr:

    x = target - i

    if x in dic:


        res += dic[x]

    if i not in dic:

        dic[i] = 1

    else:

        dic[i] +=1

print(res)
```
