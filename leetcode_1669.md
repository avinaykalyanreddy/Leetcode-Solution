#  <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 1669  
**Merge in between linked lists**. click on the link to view the [question](https://leetcode.com/problems/merge-in-between-linked-lists/description/)
### python
```python
def mergeInBetween(list1, a, b, list2):

      current = list1
      for i in range(a-1):
           current = current.next

      list1_first = current
      current = current.next

      for i in range(b-a+1):
           current = current.next

      list1_last = current

      temp = list2

      while temp.next != None:
              temp = temp.next

      list1_first.next = list2
      temp.next = list1_last

      return list1
```
**time complexity-> O(n+m)**  
**space complexity-> O(1)**  

### Output  🖥️
```
i/p->  list1 = [10,1,13,6,9,5], a = 3, b = 4, list2 = [1000000,1000001,1000002]
o/p-> [10,1,13,1000000,1000001,1000002,5]
```

  
