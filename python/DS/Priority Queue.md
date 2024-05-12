- A data structure that is like a set (at least what I understand) and works like a queue.
- We use it for setting priority of elements that are inserted.
- By default the highest priority is of the element that is the highest 
- We can change the highest priority from highest lowest using *greater* operator
- **OPERATIONS** - top, size and pop

### Complexity 
1. **Push (Insertion):** O(log n) - Inserting an element into a binary heap involves adding it at the end and then performing a "heapify-up" operation to maintain the heap property.
    
2. **Pop (Deletion of the maximum/minimum element):** O(log n) - Removing the root (max or min) element and replacing it with the last element, followed by a "heapify-down" operation to restore the heap property.
    
3. **Top (Accessing the maximum/minimum element):** O(1) - Accessing the root element, which is always the maximum or minimum in a max-heap or min-heap, respectively.
    
4. **Size (Getting the number of elements):** O(1) - Maintained as a separate variable, so retrieving the size is a constant-time operation.
    
5. **Empty (Checking if the priority queue is empty):** O(1) - Checking whether the size is zero is a constant-time operation.
    
6. **Construction (Building a priority queue from a range of elements):** O(n) - Constructing a priority queue from a range of elements can be done in linear time using the "heapify" operation.


