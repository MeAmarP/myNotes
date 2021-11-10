# Notes from grokking algorithm
## Chapter 1
### Big O Notation
- Big O notation is special notation that tells you how fast an algorithm is
- When you need to know how the running time increases as the list size increases, Big O is used.
- Big O notation lets you compare the number of operations.
- Some common Big O runtime:
    - O(log n) called as _log time_. e.g. Binary Search
    - O(n) called as _linear time_. e.g. Simple Search
    - O(n * log n)
    - O(n^2)
    - O(n!) called as _factorial time_. e.g. Traveling Salesmen 
- Key Takeaways:
    - Algorithm speed isn’t measured in seconds, but in growth of the number of operations.
    - Instead, we talk about how quickly the run time of an algorithm increases as the size of the input increases.
    - Run time of algorithms is expressed in Big O notation.
    - O(log n) is faster than O(n), but it gets a lot faster as the list of items you’re searching grows.

## Chapter 2 : Selection Sort
### Basics:
- **Array**: 
  - list of elements of same datatype stored in contiguous memory locations.
  - defined with fixed sized/length elements, hence hard to modify by appending extra items.
- **Linked list**:
  - list of items can be stored anywhere in a memory.
  - here you store the addresses of the items. bunch of random memory addresses are linked together.
