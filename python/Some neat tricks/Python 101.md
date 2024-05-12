 - Initializing a list with a predetermined element
 
```
prefix_products = [1] * n

it would give me 
prefix_products = [1,1,1,1] 
where,
number of elements = n
```

- Making a dictionary with value 'set'
```
myDict = defaultdict(set)
myDict['a'].add(1)
myDict['a'].add(3)

# myDict = {'a': {1,3}}
```
*dictionary is aka 'hash map'*

- Converting whole list to set
```
nums = [2,3,5,3]
hashSet = set(nums)
# hashset = {2,3,5} and we can find if a number exists or not

```