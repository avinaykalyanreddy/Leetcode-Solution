#  <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 142

**Linked list cycle II**. Click on the link to view the [question](https://leetcode.com/problems/linked-list-cycle-ii/description/)  
## Python  

**tortoise and hare**

1. Initialize two pointers, often referred to as "slow" and "fast," pointing to the head of the linked list.
1. Move the "slow" pointer one step at a time and the "fast" pointer two steps at a time through the linked list.
1. If the two pointers meet at some point while traversing the list, it indicates the presence of a cycle in the linked list.
1. Once the collision point is detected, reset one of the pointers (let's say "slow") to the head of the linked list and keep the other pointer ("fast") at the collision point.
1. Move both pointers one step at a time until they meet again. The meeting point will be the start of the cycle.
```python
 def detectCycle( head):

      slow = head
      fast = head

      while fast and fast.next:

            slow = slow.next
            fast = fast.next.next

            if slow == fast:

                  slow = head

                  while slow != fast:

                            slow = slow.next
                            fast = fast.next
                  return slow
      return None
```

