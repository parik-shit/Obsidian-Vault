A monotonic stack is a stack whose elements are monotonically increasing or decreasing. It contains all qualities that a typical stack has and its elements are all monotonic decreasing or increasing.

Below are the features of a monotonic stack:

- It is a range of queries in an array situation
- The minima/maxima elements
- When an element is popped from the monotonic stack, it will never be utilised again.

### Example - Daily Temperature

```class Solution:

    def dailyTemperatures(self, temperatures: List[int]) -> List[int]:

        stack = []

        n = len(temperatures)

        ans = [0] * n

        for i in range(n - 1, -1, -1):

            while stack and stack[-1][0] <= temperatures[i]:

                stack.pop()

            if len(stack) == 0:

                ans[i] = 0

            else:

                ans[i] = stack[-1][1] - i

            stack.append([temperatures[i], i])

        return ans
```

Here we are starting from ending to start 
- if the current temp > stack.top() -> then we pop the element
- if the stack is empty we set ans[i] = 0
- else: we append the current value (current temp in this case) to the stack

![[Pasted image 20240206190120.png]]