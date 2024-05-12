`Input:`
We are given two trees and we have to check if they are equal/same

`Solution`:
Just make ***base cases*** for three conditions without which the nodes of two tree will not be equal.

- `Base Case - 1`: `if not q and not p: return True`
- `Base Case - 1`: `if not q or not p: return False`
- `Base Case - 1`: `if q.val != p.val: return False`
- `return isSameTree(q.left, p.left) and isSameTree(q.right, p.right)`

