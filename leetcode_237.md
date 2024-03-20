#  <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 237  
Delete node in a linkedlist. Click on the link to view the [Question](https://leetcode.com/problems/delete-node-in-a-linked-list/description/)

### Python 
```python
class Solution:
    def deleteNode(self, node):

        node.val = node.next.val
        node.next = node.next.next

```
**Time complexity -> O(1)**  
**Space complexity -> O(1)**



