#  <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 2095

**Delete the middle node of a linkedlist**. Click on the link to view the [question](https://leetcode.com/problems/delete-the-middle-node-of-a-linked-list/description/)

## Python  

**Algorithm->** Tortoise and Hare  
```python
class Solution:
    def deleteMiddle(self, head: Optional[ListNode]) -> Optional[ListNode]:

        if head.next is None:
            return None

        slow = head
        fast = head
        prev = None

        while fast and fast.next:
            prev = slow

            slow = slow.next
            fast = fast.next.next

        prev.next = slow.next

        return head
```

Time complexity-> O(n/2) -> O(n)  

Space complexity-> O(1)

