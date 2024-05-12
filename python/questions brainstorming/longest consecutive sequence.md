> Bonus: Check in Python 101 for the set trick

>**Input:** nums = [100,4,200,1,3,2]
**Output:** 4
**Explanation:** The longest consecutive elements sequence is `[1, 2, 3, 4]`. Therefore its length is 4.

### What is the problem asking?
	we need to find the length of longest consecutive sequence 

### algo:

```
#using the trick here
hashset = set(nums)
longest = 0

for n in nums:
	if n - 1 not in hashset:
		length = 0
		while n + length in hashset:
			length += 1
		longest = max(longest,length)

return longest
```

- `if n - 1 not in hashset:` we use this to check that the element doesn't have a left neighbor, which means that element is the leader of the sequence 
- ```
while n + length in hashset:
			length += 1
		longest = max(longest,length)
```
we used this to increase length every time we find a consecutive element and after the loop is completed  update the longest (incase it is the longest)

