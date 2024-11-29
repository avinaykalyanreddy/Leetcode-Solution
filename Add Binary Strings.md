```python
class Solution:
	def addBinary(self, s1, s2):
		# code here
		if len(s1) > len(s2):
            s2  = "0"*(len(s1)-len(s2))+s2
        
        else:
        
            s1 = "0"*(len(s2)-len(s1))+s1
        
        
        res = []
        
        carry = 0
        
        for i in range(len(s1)-1,-1,-1):
        
            x = carry + int(s1[i]) + int(s2[i])
        
            carry = x//2   # 3//2 --> 1, 2//2 --> 1, 1//2 --> 0
        
            res.append(str(x%2)) # 3%2 --> 1, 2%2 --> 0, 1%2 --> 1
        
        if carry:
        
            res.append('1')
        
        return ("".join(res[::-1]).lstrip('0')) if res else "0"

```
