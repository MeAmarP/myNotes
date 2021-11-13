# Notes from grokking algorithm
## Chapter 1
---
### Binary Search
- Expects sorted list of elements as Input.
- In a given list, It returns position of the element that we are looking for, else NULL.
- Binary search only works with sorted list.
- Basically this algo search for element by repeatedly dividing the search interval in half.
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
---
### Basics:
- **Array**: 
  - list of elements of same datatype stored in contiguous memory locations.
  - fast to access and allows **random access**.
  - defined with *fixed sized/length elements*, hence hard to modify by appending extra items.
  - **RUNTIME by Operation:** READ = O(1) | INSERT = O(N) | DELETE = O(N).
- **Linked list**:
  - list of items can be stored anywhere in a memory.
  - here you store element with the memory address of the next items. bunch of random memory addresses are linked together.
  - Size is dynamic, can be change at runtime.
  - requires **sequential access**.
  - - **RUNTIME by Operation:** READ = O(N) | INSERT = O(1) | DELETE = O(1).

### Algorithm for Selection Sort:
    selectionSort(array, size)
      repeat (size - 1) times
      set the first unsorted element as the minimum
      for each of the unsorted elements
        if element < currentMinimum
          set element as new minimum
      swap minimum with first unsorted position
    end selectionSort

## Chapter 3 : Recursion
---
- Recursion is when a function calls itself.
- Every recursive function has *Base Case* and *Recursive Case*.
### Stack
- All function calls go onto the call stack.
- A stack has pop and push operations.
- The call stack can get very large, which takes up a lot of memory.

## Chapter 4 : Quicksort
---
- This algo approaches sorting problem by using **Divide & Conquer** technique.
- Much faster then Selection sort.
### Algorithm for  Quick Sort:
- An array is divided into sub-arrays by selecting a pivot element.
- While dividing the array the pivot element should be positioned in such a way that elements less then pivot are on left and elements greater then pivot are on right.
- These left and right sub-arrays are also further divided by similar technique, until we have single element in each of sub-array.
