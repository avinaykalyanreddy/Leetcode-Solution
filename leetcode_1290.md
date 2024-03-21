#  <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 1290

*Convert binary number in linked list to integer**. Click on the link to view the [question](https://leetcode.com/problems/convert-binary-number-in-a-linked-list-to-integer/description/)

**Explaination**  
1. We start solving the binary number from right (index 0) to left (index n-1), where n is the number of digits in the binary number.
2. For example, let's consider the binary number 1101.
3. When the base is 2, the formula to convert a binary number to decimal is: 1* 2^3 + 1* 2^2 + 0* 2^1 + 1* 2^0
## Python  

```python
class Solution:
    def getDecimalValue(self, head: ListNode) -> int:
        temp1 = None; temp2 = None
        while head.next:

            temp1 = head.next
            head.next = temp2
            temp2 = head

            head = temp1

        head.next  = temp2


        res = 0
        i = 0


        while(head):

            res = res + head.val*2**i
            i = i+1
            head = head.next

        return res

```

Time complexity -> O(n)  
Space complexity-> O(1)

