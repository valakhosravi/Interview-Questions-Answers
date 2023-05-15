**Q: What is a data structure?**  
A data structure is a way of organizing and storing data in a computer so that it can be accessed and used efficiently.

**Q: What is an algorithm?**  
An algorithm is a set of instructions that describe how to perform a specific task or solve a particular problem.

**Q: What is the difference between an array and a linked list?**  
An array is a collection of elements stored in contiguous memory locations. A linked list is a collection of elements that are linked together using pointers. The main difference is that inserting or deleting an element in an array can be time-consuming, while inserting or deleting an element in a linked list is much faster.

**Q: What is a stack?**  
A stack is a data structure that stores elements in a last-in-first-out (LIFO) order. The two main operations on a stack are push (add an element to the top of the stack) and pop (remove the top element from the stack).

**Q: What is a queue?**  
A queue is a data structure that stores elements in a first-in-first-out (FIFO) order. The two main operations on a queue are enqueue (add an element to the back of the queue) and dequeue (remove the front element from the queue).

**Q: What is a binary search tree?**  
A binary search tree is a data structure that is used to store a collection of elements in a way that allows for efficient search, insertion, and deletion. Each node in the tree has at most two children, and the left child is always smaller than the parent node, while the right child is always larger.

**Q: What is a hash table?**  
A hash table is a data structure that stores key-value pairs. It uses a hash function to compute an index into an array of buckets, where the value associated with the key is stored. The main advantage of a hash table is that it provides constant-time access to the values.

**Q: What is a sorting algorithm?**  
A sorting algorithm is an algorithm that puts elements of a list in a certain order. The most common sorting algorithms are bubble sort, insertion sort, selection sort, quicksort, mergesort, and heapsort.

**Q: What is dynamic programming?**  
Dynamic programming is a technique used to solve problems by breaking them down into smaller subproblems and solving each subproblem only once. The solutions to the subproblems are then stored in a table and used to solve the larger problem.

**Q: What is the time complexity of an algorithm?**  
The time complexity of an algorithm is a measure of the amount of time it takes to run as a function of the input size. It is typically expressed using big O notation, which gives an upper bound on the growth rate of the function.

**Q: What is the difference between a greedy algorithm and a dynamic programming algorithm?**  
A greedy algorithm makes the locally optimal choice at each step, hoping to find a global optimum. A dynamic programming algorithm, on the other hand, solves problems by breaking them down into smaller subproblems and solving each subproblem only once.

**Q: What is the time complexity of a bubble sort algorithm?**  
The time complexity of a bubble sort algorithm is O(n^2), where n is the number of elements in the list.

**Q: What is the time complexity of a binary search algorithm?**  
The time complexity of a binary search algorithm is O(log n), where n is the number of elements in the sorted list.

**Q: What is the time complexity of a merge sort algorithm?**  
The time complexity of a merge sort algorithm is O(n log n), where n is the number of elements in the list.

**Q: What is the difference between an in-place sorting algorithm and a not-in-place sorting algorithm?**  
An in-place sorting algorithm sorts the list by modifying the positions of the elements in the list, without creating a new copy of the list. A not-in-place sorting algorithm creates a new copy of the list and sorts the copy.

**Q: What is memoization?**  
Memoization is a technique used to speed up dynamic programming algorithms by caching the results of expensive function calls and returning the cached result when the same inputs occur again.

**Q: What is the time complexity of a linear search algorithm?**  
The time complexity of a linear search algorithm is O(n), where n is the number of elements in the list.

**Q: What is the difference between a breadth-first search and a depth-first search?**  
A breadth-first search explores all the nodes at a given depth before moving on to the next depth. A depth-first search explores as far as possible along each branch before backtracking.

**Q: What is a backtracking algorithm?**  
A backtracking algorithm is an algorithm that searches for all possible solutions to a problem by trying out all possible choices and undoing the choices that do not lead to a solution.

**Q: What is the time complexity of a quicksort algorithm?**  
The time complexity of a quicksort algorithm is O(n log n) on average, but can be O(n^2) in the worst case.

**Q: Write a function to find the maximum sum of any contiguous subarray in a given array of integers.**  
```python
def max_subarray_sum(arr):
    max_sum = float('-inf')
    current_sum = 0

    for num in arr:
        current_sum = max(num, current_sum + num)
        max_sum = max(max_sum, current_sum)

    return max_sum

# Test the function
arr = [1, -3, 2, 1, -1]
print(max_subarray_sum(arr))  # Output: 3 (corresponding to subarray [2, 1])
```

**Q: Implement a function to reverse a singly linked list.**  
```python
class ListNode:
    def __init__(self, val=0, next=None):
        self.val = val
        self.next = next

def reverse_linked_list(head):
    prev = None
    current = head

    while current:
        next_node = current.next
        current.next = prev
        prev = current
        current = next_node

    return prev

# Test the function
head = ListNode(1)
head.next = ListNode(2)
head.next.next = ListNode(3)
reversed_head = reverse_linked_list(head)
print(reversed_head.val, reversed_head.next.val, reversed_head.next.next.val)  # Output: 3 2 1
```

**Q: Given a sorted array of integers, write a function to remove all duplicate elements in-place and return the new length of the array.**  
```python
def remove_duplicates(nums):
    if len(nums) == 0:
        return 0

    unique_index = 0
    for i in range(1, len(nums)):
        if nums[i] != nums[unique_index]:
            unique_index += 1
            nums[unique_index] = nums[i]

    return unique_index + 1

# Test the function
nums = [1, 1, 2, 2, 2, 3, 4, 4, 5]
new_length = remove_duplicates(nums)
print(new_length)  # Output: 5 (corresponding to the array [1, 2, 3, 4, 5])
```

**Q: Implement a function to check whether a string is a palindrome (reads the same forwards and backwards), considering only alphanumeric characters and ignoring case.**  
```python
import re

def is_palindrome(s):
    s = re.sub('[^a-zA-Z0-9]', '', s).lower()
    return s == s[::-1]

# Test the function
string1 = "A man, a plan, a canal: Panama"
string2 = "race a car"
print(is_palindrome(string1))  # Output: True
print(is_palindrome(string2))  # Output: False
```

