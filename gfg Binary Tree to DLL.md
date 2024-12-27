### Given a Binary Tree (BT), convert it to a Doubly Linked List (DLL) in place. The left and right pointers in nodes will be used as previous and next pointers respectively in converted DLL. The order of nodes in DLL must be the same as the order of the given Binary Tree. The first node of Inorder traversal (leftmost node in BT) must be the head node of the DLL.


```python
'''
class Node:
    """ Class Node """
    def __init__(self, value):
        self.left = None
        self.data = value
        self.right = None
'''
class Solution:
    def bToDLL(self,root):
        
        self.res = None
        self.prev = None
        
        def inorder(root):
            
            if root:
                
                return root 
            
            inorder(root.left)
            
            if not self.res:
                
                self.res = root
                
            if self.prev:
                
                self.prev.right = root
                
                root.left = self.prev
            
            self.prev = root
            
            inorder(root.right)
            
            
            
        
        inorder(root)
        
        return self.res

```

time complexity : O(n)
space complexity : O(H)



