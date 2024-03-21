#  <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 203  
**Remove linked list elements**. Click on the link to view the [question](https://leetcode.com/problems/remove-linked-list-elements/description/)  

## Python  

1. Start by pointing a temporary variable temp to the head of a linked list.
1. Also, have another variable prev initially set to None, which will track the previous node as we traverse the list.
2. Now, we loop through the list until temp becomes None (indicating the end of the list).
3. Inside the loop:
   - Check if the value of the current node (temp.val) is equal to the value we want to remove (val).
   - If it is:
       * If the node is the head of the list (temp == head), then update head to point to the next node (head = head.next).
       * If it's not the head, then adjust the next pointer of the previous node (prev.next) to skip over the current node (temp.next), effectively removing it from the list.
       * Move temp to the next node (temp = temp.next).
    - If the value doesn't match, update prev to temp and move temp to the next node.
      
1. now return the head

```python
class Solution:
    def removeElements(self, head: Optional[ListNode], val: int) -> Optional[ListNode]:

          prev = None
          temp = head

          while temp:

                if temp.val == val:

                      if temp == head:

                            head = head.next

                      else:

                              prev.next = temp.next
                      temp = temp.next
                else:
                      prev = temp
                      temp = temp.next
                
        
          return head
```
**time complexity-> O(N)**  
**space complexity -> O(1)**



 




