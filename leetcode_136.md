# <img src="https://leetcode.com/_next/static/images/logo-ff2b712834cf26bf50a5de58ee27bcef.png" alt="LeetCode Logo" width="50" height="80"> Leetcode problem -> 136

Click no the link to view the [Question](https://leetcode.com/problems/single-number/description/?envType=study-plan-v2&envId=leetcode-75)

## Python
```python

def singleNumber(nums):

      res = 0
      for i in nums:
          res = res^i
      return res

singleNumber([4,1,2,1,2])
```
## Output
```
4
```
## Explaination

##### NOTE -> As we see from the question except one element, remaining elements repeats twice. Above code won't work  if element repeats more than twice.

 let us understand XOR(^) operator

 if two bit's are same then it is set to  0 and if bit's are different set to 1.

<img src="https://shorturl.at/qrsu7" >

### print(2^2) -> 0
because binary number of 2 is  **0010**

0010 -> 2  
0010 -> 2

0000 -> 0 --------- equation1

compare each bit from right to left , result will be 0 this is how XOR(^) operator works

binary number for 4 is  0100

### print(equation1 ^ 4)  

0000 -> 0  
0100 -> 4  

---------   
0100 -> 4

this how above code works


    

