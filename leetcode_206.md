#  <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 206

**Reverse linked list**. Click on the link to view the [question](https://leetcode.com/problems/reverse-linked-list/description/)  

<img src="https://media.giphy.com/media/coxQHKASG60HrHtvkt/giphy.gif?cid=790b76116dksp1lj18yfvjqxe22lrdsdqmpcxcmjldsmb1dx&ep=v1_gifs_search&rid=giphy.gif&ct=g" height="150" width="1000">  

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
