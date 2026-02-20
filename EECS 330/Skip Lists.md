# Linked List

## Overview
A linked list is a linear data structure where elements are dynamically allocated in memory and do not reside in contiguous locations. Each element is called a node and contains data alongside a pointer to the next node. 


[Image of a singly linked list]


## Types
* **Singly Linked List:** Nodes contain a data field and a single pointer to the next node.
* **Doubly Linked List:** Nodes contain a data field, a pointer to the next node, and a pointer to the previous node. 

* **Circular Linked List:** The final node's next pointer references the first node, creating a closed loop.

## Time Complexity
Linked lists provide efficient insertions and deletions when the target node is known but are inefficient for searching.
* [cite_start]**Search:** $O(n)$ for both sorted and unsorted linked lists[cite: 25, 318].
* [cite_start]**Insert (Unsorted):** $\Theta(1)$[cite: 318].
* [cite_start]**Insert (Sorted):** $O(n)$ to locate the correct insertion point [cite: 26][cite_start], followed by $\Theta(1)$ to execute the insertion[cite: 27].
* [cite_start]**Delete:** $O(n)$ overall[cite: 318], consisting of $O(n)$ search time and $\Theta(1)$ pointer reassignment.

## Memory Implications
Memory is allocated on the heap per node. This introduces overhead for the pointer storage and can lead to poor CPU cache locality compared to array allocations.

## C Implementation Node
```c
struct Node {
    int data;
    struct Node* next;
};