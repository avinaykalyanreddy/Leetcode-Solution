#### Given two sorted arrays a[] and b[] of size n and m respectively, the task is to merge them in sorted order without using any extra space. Modify a so that it contains the first n elements and modify b so that it contains the last m elements.

```
Input: a[] = [2, 4, 7, 10], b[] = [2, 3]
Output:
2 2 3 4
7 10
Explanation: After merging the two non-decreasing arrays, we get, 2 2 3 4 7 10
```

```
Input: a[] = [1, 5, 9, 10, 15, 20], b[] = [2, 3, 8, 13]
Output:
1 2 3 5 8 9
10 13 15 20
Explanation: After merging two sorted arrays we get 5 10 12 18 20
```

### Algorithm

1. My logic is that all elements in array 'a' should be less than or equal to array 'b'
2. **Initialize pointers:** 
   * Start from end of the array a (len(a) - 1)
   * Start from beginning of the array b( 0 )
3. **Compare and Swap**
   * Compare largest element of a (pointed by i) with smallet element of b (pointed by j)
   * if the element a is > element b  
      * swap the two elements
      * move pointer i = i-1
      * move pointer j = j+1
   * if the element a is not greater than element b than stop the comparison process because the both array is sorted  

4. **Sort both arrays**  
      * sort a and b using sort( )
   

### Explaination  

```python
a = [1, 3, 5, 7]
b = [0, 2, 6, 8, 9]
```

1. Compare a[3] = 7 with b[0] = 0.  
   * Since 7 > 0 , now swap the values.
   * a = [1, 3, 5, 0] b = [7, 2, 6, 8, 9]

2. Compare a[2] = 5 with b[1] = 2.  
   * since 5 > 2, now swap the values.
   * a = [1, 3, 2, 0] b = [7, 5, 6, 8, 9]

3. Compare a[1] = 3 with b[2] = 6.  
   * 3 < 6 no more swaps are needed. Break the loop.

4. a.sort() and b.sort()  
   * a = [0,1,2,3]
   * b = [5,6,7,8,9]

```python
a  = [2,4,7,10]; b = [2,3 ]
i = len(a) - 1
j = 0

while i > -1 and j < len(b): 
    
   if a[i] > b[j]:
      
      a[i],b[j] = b[j],a[i]
      
      i = i - 1
      j += 1
      continue
      
    break
   
a.sort()
b.sort()

print(a,b)

```


Time Complexity : O(nlog(n))  
Space Complexity : O(1)

 





