### What is the problem asking ?
	find the combination of the numbers that add up to 'k'
	note: the answer will unique (i.e only 1 combination exists)

## algo:

```
hashmap = {}
for i,n in enumerate(nums):
	diff = k - n
	if diff in hashmap:
		return [hashmap[diff], i]
	hashmap[n] = i
```

basically storing the number as the ***key***  and its ***index*** as the value