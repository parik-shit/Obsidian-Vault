#### What is given ?
- Two sorted lists
#### What are we supposed to find ?
Median 

###### Median:
even number of observations = ![[Pasted image 20240225150630.png]]
odd number of observations = ![[Pasted image 20240225150705.png]]
```
A = [1,3,4,6,9] , B = [2,3,4,8,10]
[1,2,3,3,4,4,6,8,9,10]
m1 = 4 
m2 = 4
```
Therefore, the middle elements are **m1** and **m2** in the sorted array (m1 and m2 are medians of A and B respectively)

#### Case 1: if (m1 == m2):
- m1 and m2 will be the middle elements in the merged and sorted array
#### Case 2: if (m1 < m2):
- 