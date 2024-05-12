Recursive approach, with each recursive call we go till the end of the given linked list (***tail recursion***). While returning (popping frames) we set the `next.next` of the current node to the current node (`head.next.next`) and `head.next = None`

### What is problem asking ?
Reverse the given linked list 

### algo:

```
def reverseList(self, head):
	if not head:
		return None
	newHead = head
	if head.next:
		newHead = self.reverseList(head.next)

	head.next.next = head
	head.next = None
	return newHead			 			
```

![[Pasted image 20240330202442.png]]