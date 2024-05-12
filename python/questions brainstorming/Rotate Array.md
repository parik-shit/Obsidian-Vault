#### TC: `O(N)` SC: `O(1)`

##### Input:
`arr = [1,2,3,4,5]`
`k = 2`

##### Output:
`arr = [4,5,1,2,3]`

The method that I'm going to use, will use constant space

given an array and an integer 'k', we are supposed to rotate the array 'k' times

### Intuition:
`k = k % len(array)`
with this piece of code we have achieved:
- If `k < len(array)` then rotate k times
- If `k > len(array)` then rotate (0 + remainder of 5/3 ) times
- If `k = len(array)` then rotate 0 times
