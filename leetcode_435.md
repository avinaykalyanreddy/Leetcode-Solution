# <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 435

Non-overlapping Intervals. Click on the link to view the [Question](https://leetcode.com/problems/non-overlapping-intervals/description/?envType=study-plan-v2&envId=leetcode-75)  

# Python
```python
def eraseOverlapIntervals(intervals):

      intervals.sort(key = lambda a: a[1])
      high = intervals[0][0]

      res = 0
      for i in intervals[1::]:

            if intervals[0] < high:
                res = res+1
            else:
                high = i[1]
      return 1

eraseOverlapIntervals(intervals = [[1,2],[2,3],[3,4],[1,3]])
```
# Output 🖥️
```
1
```
