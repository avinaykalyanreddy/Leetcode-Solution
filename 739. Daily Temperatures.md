**Given an array of integers temperatures represents the daily temperatures, return an array answer such that answer[i] is the number of days you have to wait after the ith day to get a warmer temperature. If there is no future day for which this is possible, keep answer[i] == 0 instead.**  

```
Example 1:

Input: temperatures = [73,74,75,71,69,72,76,73]
Output: [1,1,4,2,1,1,0,0]
```

```
Example 2:

Input: temperatures = [30,40,50,60]
Output: [1,1,1,0]
```

# Algorithm:

1. Initialize   
    * Create a list res of size 
𝑛
n (length of temperatures) filled with zeros. This will store the result.
    * Create a empty list stack to store the indices of temperature.

2. Traverse the temperatures Array Backwards:  
    * Traverse from the last index and move to the first.

3. Process Each Temperature:  
    * While the stack is not empty and the temperature at the index stored at the top of the stack is less than or equal to the current temperature:  
        * Pop the index from the stack (these indices represent temperatures that won't be the "next warmer day" for the current day).

4. Calculate the Next Warmer Day:  
    * If the stack is not empty, the index at the top of the stack represents the next warmer day for the current day:  
        * Calculate the difference between the two indices and store it in res[i].

5. Push the Current Index onto the Stack:  
   * Add the current index to the stack so it can be considered for future days.

6. Return the Result...

```python
temperatures = [73,74,75,71,69,72,76,73]

res = [0]*len(temperatures)

stack = []

for i in range(len(temperatures)-1,-1,-1):
    
    while stack and  temperatures[stack[-1]] <= temperatures[i]:
        
        stack.pop()
        
    
    if len(stack) != 0:
            
            res[i] = stack[-1] - i
            
    stack.append(i)
        
print(res)

```


