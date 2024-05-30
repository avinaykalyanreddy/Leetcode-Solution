#  <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 102  

Binary Tree Level Order Traversal. Click on the link to view the [question](https://leetcode.com/problems/binary-tree-level-order-traversal/description/)  


### Python  
Binary Tree Level Order Traversal is a BFS 
```python

# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right

class Solution:
    def levelOrder(self, root: Optional[TreeNode]) -> List[List[int]]:

          parent = [root]
          result = []
          while len(parent):

              child = []
              res = []
              for node in parent:

                  if node != None:

                          res.append(node.val)
                          if node.left:
                                child.append(node.left)
                          if node.right:
                                child.append(node.right)
                  if res:
                        result.append(res)
                  parent = child
          return result

```







