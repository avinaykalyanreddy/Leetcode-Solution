#  <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 206

**Reverse linked list**. Click on the link to view the [question](https://leetcode.com/problems/reverse-linked-list/description/)  

<img src="https://i.pinimg.com/736x/cc/01/40/cc014030afd5a3e5283ee0c175e36362.jpg" height="150" width="1000">  

```python

def reverseList(head) :

      if head == None or head.next == None:
                    return head

      temp1 = None;temp2 = None

      while(head.next != None):

            temp1 = head.next
            head.next = temp2
            temp2 = head
            head = temp1

      head.next = temp2
      return head
```

**Space complexity-> O(1)**  
**time complexity-> O(n)**
