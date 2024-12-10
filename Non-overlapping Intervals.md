#### Given a 2D array intervals[][] of representing intervals where intervals [i] = [starti, endi ]. Return the minimum number of intervals you need to remove to make the rest of the intervals non-overlapping.  

```
Input: intervals[][] = [[1, 2], [2, 3], [3, 4], [1, 3]]
Output: 1
Explanation: [1, 3] can be removed and the rest of the intervals are non-overlapping.
```

### Approch 
* Sort the the given array based on end time because next interval should start after the previous interval end time.
* This problem is solved by greedy approach where each time selecting optimal choice.

```python
intervals = [[1, 2], [2, 3], [3, 4], [1, 3]]
intervals.sort(key=lambda a: a[1])
end = float("-inf")

count = 0

for  start,e in intervals:
    
    if start  < end:
        
        count += 1
        
    else:
        
        end = e
        
print(count)


```

Time complexity --> O(nlog(n))  
Space complexity --> O(1)
