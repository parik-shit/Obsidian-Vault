```
def walk(tree):
    if tree is not None:
        print(tree)
        walk(tree.left)
        walk(tree.right)
```
