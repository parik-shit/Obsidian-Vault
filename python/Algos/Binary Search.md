- The list should be sorted
- Declare a `high = len(array) -1` and `low = 0`
- `mid = (high + low)/2`
## code:
```
def binary_search(arr, key):
    s = 0
    e = len(arr) - 1
    while s <= e:
        mid = (s + e) // 2
        if arr[mid] == key:
            return mid
        if key < arr[mid]:
            e = mid - 1
        else:
            s = mid + 1
    return -1
```

> If the loop returns `mid` it means it has found the element else it will `return -1` 