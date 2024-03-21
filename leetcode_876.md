#  <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 876  
**Middle of the linked list**. Click on the link to view the [Question](https://leetcode.com/problems/middle-of-the-linked-list/description/)  

## Python

**My approch**
```python
class Solution:
    def middleNode(self, head: Optional[ListNode]) -> Optional[ListNode]:
        
        count = 0

        temp = head

        while temp:

            count = count+1
            temp = temp.next

        temp = head

        for i in range(count//2):

            temp = temp.next

        return temp

        
```
**Anonymous approach**

```python

class Solution:
    def middleNode(self, head: Optional[ListNode]) -> Optional[ListNode]:

        if head is None and head.next is None:
            return head

        
        slow = head
        fast = head

        while fast and fast.next:

            slow = slow.next
            fast = fast.next.next

        return slow

# for even list fast ends with None
# for odd list fast ends with last element
```

In both cases time complexity is O(n) and space complexity O(1) but 2nd case is more efficient.

