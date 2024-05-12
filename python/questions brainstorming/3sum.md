For this problem we will be using ***2 pointers*** algo

### What is problem asking ?
Given a list of integers, find the triplets which are == 0 and also there should be no duplicates

### algo:

```
res = []
nums.sort

for i,n in enumerate(nums):
	if i > 0 and nums[i-1] == nums[i]:
		continue
	
	r = len(nums) - 1
	l = i + 1
	while l < r:
		currSum = n + nums[l] + nums[r]
		if currSum > 0:
			r -=1
		elif currSum < 0:
			l += 1
		else:
			res.append([n,nums[l],nums[r]])
			l += 1
			while nums[l] != nums[l - 1]:
				l+=1
return res
				 			
```

first we sort the list to use 2 pointer approach

conditions that we have to check 
we have used a for loop in which we are going to check if the current element != to the previous element for which we have to see that the index of the current element > 0
`if i > 0 and nums[i] == nums[i-1]: continue`

then we have a while loop:
	in the while loop `l = 0 and r = len(nums) - 1`
then we use a variable to store the current sum:
	`currSum = nums[i] + nums[l] + nums[r]`
	```if currSum > 0:
			r -=1
		elif currSum < 0:
			l += 1
		else:
			res.append([n,nums[l],nums[r]])
			l += 1
			while nums[l] != nums[l - 1]:
				l+=1

we are also doing the same check for the 'l' pointer too. This is done to prevent duplicate elements in the triplets