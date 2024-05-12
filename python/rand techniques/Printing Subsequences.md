![[Pasted image 20240106213450.png]]

```
def walk(tree):
    if tree is not None:
        print(tree)
        walk(tree.left)
        walk(tree.right)
```