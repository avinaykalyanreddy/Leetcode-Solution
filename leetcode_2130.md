#  <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 2130  
**Maximum Twin Sum of a Linked List**. Click on the link to view the [question](https://leetcode.com/problems/maximum-twin-sum-of-a-linked-list/description/)

## Python

```python
class Solution:
    def pairSum(self, head: Optional[ListNode]) -> int:

        array = []

        while head:

            array.append(head.val)
            head = head.next

        l = 0
        r = len(array)-1
        ans = 0
        while(l<r):

            ans = max(ans,array[l]+array[r])

            l = l+1
            r = r-1

        return ans

```

Time complexity -> O(n)  
Space complexity -> O(n)

**another approach algo**  
1. slow and fast variables

1. find middle node by using Tortoise and Hare algorithm  

1. after finding middle node cur = slow and slow = slow.next
2. now reverse the slow variable
3. now declare sum = 0
4. use while loop (slow):
     - sum = max(sum,cur.val+slow.val)
     - cur = cur.next
     - slow = slow.next
1. now return the sum
       
Time complexity-> O(n)  

Space complexity-> O(1)
   
